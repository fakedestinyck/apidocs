# Spider
边缘应用，西南节点

## 说明
更新common公告库至最新版  
`npm install @jx3box/jx3box-common`
1. 前端接口地址引入请统一使用
```javascript
const {JX3BOX} = require('@jx3box/jx3box-common')
const API = JX3BOX.__server + path
```
2. 服务器数据引用请使用
```javascript
const yourdata = require('@jx3box/jx3box-common/data/server')
```

## 开服状态
GET https://spider.jx3box.com/jx3servers  
[服务器数据说明](https://github.com/JX3BOX/jx3box-common/blob/master/data/server.json)

## 金价数据
GET https://spider.jx3box.com/jx3price  
[服务器数据说明](https://github.com/JX3BOX/jx3box-common/blob/master/data/server.json)