#browserlist で last N versionに何が含まれているか確認する方法

##code
`cd PATH_TO_browserlist_DIRECTORY`  
で、node cli.jsする。  
`node cli.js  "last 4 versions"`  
`node cli.js  "last 3 versions"`  
`node cli.js  "last 2 versions"`  

##2015/11/26時点のそれぞれの出力
* **last 2 version**  
chrome 46
chrome 45
edge 13
edge 12
firefox 42
firefox 41
ie 11
ie 10
ie_mob 11
ie_mob 10
ios_saf 9.0-9.1
ios_saf 8.1-8.4
opera 33
opera 32
safari 9
safari 8
***

* **last 4 version**  
chrome 46
chrome 45
chrome 44
chrome 43
edge 13
edge 12
firefox 42
firefox 41
firefox 40
firefox 39
ie 11
ie 10
ie 9
ie 8
ie_mob 11
ie_mob 10
ios_saf 9.0-9.1
ios_saf 8.1-8.4
ios_saf 8
ios_saf 7.0-7.1
opera 33
opera 32
opera 31
opera 30
safari 9
safari 8
safari 7.1
safari 7
***

* **`node cli.js  "last 2 version, safari 5, ie 8, ie 9, ff 17, opera 12.1, ios 6, android 4"`**  
android 4
chrome 46
chrome 45
edge 13
edge 12
firefox 42
firefox 41
firefox 17
ie 11
ie 10
ie 9
ie 8
ie_mob 11
ie_mob 10
ios_saf 9.0-9.1
ios_saf 8.1-8.4
ios_saf 6.0-6.1
opera 33
opera 32
opera 12.1
safari 9
safari 8
safari 5

ふむ。

