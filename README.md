blog
=========

《nodejs开发指南》微博实例express4.x版

1、官网下载MongoDB

2、运行MongoDB：

   在MongoDB文件夹下创建data文件夹

   app.js--->
   store: new MongoStore({
                     db: settings.db
             })
             改成
             store: new MongoStore({
                     url:'mongodb://localhost/' + settings.db,
                     autoRemove:'native'
             })

   db.js--->Connection.DEFAULT_PORT改成27017
   在新建一个MongoDB新建一个data文件夹

   First:
   命令行：
   D:\Mongodb\bin>mongod --dbpath D:\Mongodb\data

   Second:
   按照安装位置的不同修改启动博客mongodb.bat批处理文件

   运行:app.js

   网站打开:localhost:3000

   注:指定mongodb的服务端口号为10001      mongod --dbpath D:\Mongodb\data --port 10001(express报错)

