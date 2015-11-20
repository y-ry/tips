#node.js expressでcsrfを使う。

##前提
express 4.x系

##インストールとrequier
`npm install csurf --save`

##サンプル app.js
var cookieParser = require('cookie-parser')
var csrf = require('csurf');//csrf
var bodyParser = require('body-parser')
var express = require('express')

// setup route middlewares 
var csrfProtection = csrf({ cookie: true })
var parseForm = bodyParser.urlencoded({ extended: false })

// create express app 
var app = express()

// parse cookies 
// we need this because "cookie" is true in csrfProtection 
app.use(cookieParser())

app.get('/form', csrfProtection, function(req, res) {
// pass the csrfToken to the view 
res.render('send', { csrfToken: req.csrfToken() })
})

app.post('/process', parseForm, csrfProtection, function(req, res) {
res.send('data is being processed')
})

##サンプル view(ejs)
_csrfをhiddenで与えてあげる
<form action="/process" method="POST">
<input type="hidden" name="_csrf" value="<%= csrfToken %>">

Favorite color: <input type="text" name="favoriteColor">
<button type="submit">Submit</button>
</form>




