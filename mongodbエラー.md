#mongodbの`mongo`コマンドでエラーになる場合

##発生するエラー
    $ mongo
    MongoDB shell version: 3.0.7
    connecting to: test
    2015-11-19T00:40:24.400+0900 W NETWORK  Failed to connect to 127.0.0.1:27017, reason: errno:61 Connection refused
    2015-11-19T00:40:24.402+0900 E QUERY    Error: couldn't connect to server 127.0.0.1:27017 (127.0.0.1), connection attempt failed
    at connect (src/mongo/shell/mongo.js:179:14)
    at (connect):1:6 at src/mongo/shell/mongo.js:179
    exception: connect failed

##まずはrepairしてみる。
`sudo mongod --repair`してあげる

##repair出来なかった場合
/data/dbがないよと怒られる。。。
    I STORAGE  [initandlisten] exception in initAndListen: 29 Data directory /data/db not found., terminating
    I CONTROL  [initandlisten] dbexit:  rc: 100

####mongodbのデータファイル場所に該当ファイルを作ってあげる。
`sudo mkdir -p /data/db`
(http://kzy52.com/entry/2013/07/15/224721)

###データファイルディレクトリを別の場所にしている場合は、以下のurl参考に、よきに計らえる。
(http://qiita.com/hidesuke/items/56a87d827708c8c770da)




