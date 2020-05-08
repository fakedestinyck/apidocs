# IDB
前端IndexedDB数据库接口
默认使用**jx3box**数据库下**posts**仓库。

```javascript
import IDB from '@jx3box/jx3box-common/js/idb'
const DB = new IDB();
DB.ready().then(() => {
    DB.setItem('key','val')
})
```

指定其它数据库或表
```javascript
const DB = new IDB(dbname,storename)
```

CURD,均返回promise
```javascript
DB.getItem(key,val)
DB.setItem(key,val)
DB.removeItem(key)
DB.clear()
```
[更多信息](https://localforage.docschina.org/#localforage)