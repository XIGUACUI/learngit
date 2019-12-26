## **MBook**
基于微信小程序的在线免费小说的应用，借助微信小程序的便捷特性，为用户提供快速，并且舒适的阅读体验。

### **运行**
#### 使用`wept`启动小程序
```
npm i wept -g
cd 微信小程序所在目录
wept -p 3100
```
启动之后直接在浏览器里打开`localhost:3100`并启用手机调试模式就好了。

#### 启动后台接口
```
# 启动mongodb
mongod --config=E:\mongod_install\mongod.conf

# 启动redis
redis-server.exe redis.windows.conf

# 启动接口
cd api
node .

```

## **爬虫**
#### 设置程序的执行时间
使用的是node的node-schedule，具体的你可以参考官网[node-schedule](https://www.npmjs.com/package/node-schedule#recurrence-rule-scheduling)

```
var schedule = require('node-schedule');

var j = schedule.scheduleJob('42 * * * *', function(){
  console.log('The answer to life, the universe, and everything!');
});
```
  + 格式：
```
*    *    *    *    *    *
┬    ┬    ┬    ┬    ┬    ┬
│    │    │    │    │    |
│    │    │    │    │    └ day of week (0 - 7) (0 or 7 is Sun)
│    │    │    │    └───── month (1 - 12)
│    │    │    └────────── day of month (1 - 31)
│    │    └─────────────── hour (0 - 23)
│    └──────────────────── minute (0 - 59)
└───────────────────────── second (0 - 59, OPTIONAL)
```


### **目录说明**

```
api --- 提供后台接口
  |-common --- loopback的公共模型
  |-server --- loopback的服务器模型
    |- boot --- 初始化执行脚本
    |- modle --- 所有定义的模型目录
    |- datasources.json --- 数据源定义文件
      |- middleware.json --- 中间件配置文件
      |- modle-config.json --- 模型定义文件
      |- server.js --- 主程序
reptile --- 所有的爬虫目录
  |- connectDB --- 连接数据库，操作数据库方法类
  |- tools --- 实用方法类
  |- networkReptile.js --- 爬虫主程序
  |- config.js --- 爬虫配置js
weixin --- 微信小程序目录
  |- assets --- 静态资源文件
  |- datas --- 静态数据
  |- images --- 图片资源文件
  |- page --- 所有微信小程序的页面
  |- util --- 工具类
  |- app.js --- 微信小程序入口文件
```


### **项目截图**
<div>
<img src="https://fs.andylistudio.com/1521214550813.png" alt="" style="width: 250px; height: auto">
<img src="https://fs.andylistudio.com/1521214553929.png" alt="" style="width: 250px; height: auto">
<img src="https://fs.andylistudio.com/1521214558128.png" alt="" style="width: 250px; height: auto">
<img src="https://fs.andylistudio.com/1521214565101.png" alt="" style="width: 250px; height: auto">
<img src="https://fs.andylistudio.com/1521214567465.png" alt="" style="width: 250px; height: auto">
<img src="https://fs.andylistudio.com/1521214571074.png" alt="" style="width: 250px; height: auto">
<img src="https://fs.andylistudio.com/1521214572862.png" alt="" style="width: 250px; height: auto">
<img src="https://fs.andylistudio.com/1521214576135.png" alt="" style="width: 250px; height: auto">
<img src="https://fs.andylistudio.com/1521214578084.png" alt="" style="width: 250px; height: auto">
<img src="https://fs.andylistudio.com/1521214580699.png" alt="" style="width: 250px; height: auto">
<img src="https://fs.andylistudio.com/1521214583072.png" alt="" style="width: 250px; height: auto">
<img src="https://fs.andylistudio.com/1521214585790.png" alt="" style="width: 250px; height: auto">
</div>
