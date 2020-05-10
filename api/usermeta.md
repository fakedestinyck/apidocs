# Usermeta

## 查询
### Request Schema
GET https://server.jx3box.com/user/meta

params_key|value_type|ex
---|---|---
uid | int | 8
key | varchar或'' | jx3_servers 

全部meta_key说明见[用户附表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_usermeta.md)

### Response Schema
#### 指定key时返回单个字段值
```json
{
    "msg": "用户字段查询成功",
    "code": 10050,
    "data": {
        "uid": "8",
        "key": "jx3_servers",
        "value": "晴昼海,鹰击长空"
    }
}
```

#### 不指定key时返回全部字段
```json
{
    "msg": "用户字段查询成功",
    "code": 10050,
    "data": {
        "uid": "8",
        "meta": {
            "jx3_servers": "晴昼海,鹰击长空",
            "favicon": "1,2,3"
        }
        
    }
}
```

## 设置

### Request Schema
POST https://server.jx3box.com/user/meta

body json key|value_type|ex
---|---|---
uid | int | 8
key | varchar | jx3_servers 
value | varchar | "晴昼海,鹰击长空" 
meta | object | key-val pair 

全部meta_key说明见[用户附表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_usermeta.md)

### Response Schema
#### 设置单个字段
```json
{
    "msg": "用户字段修改成功",
    "code": 10052,
    "data": {
        "uid": "8",
        "key": "jx3_servers",
        "value": "晴昼海"
    }
}
```

#### 设置多个字段
```json
{
    "msg": "用户字段修改成功",
    "code": 10052,
    "data": {
        "uid": "8",
        "meta": {
            "jx3_servers": "晴昼海",
            "favicons":"4,5,6"
        }
    }
}
```