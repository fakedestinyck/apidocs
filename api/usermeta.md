# Usermeta

## 查询
### Request Schema
GET https://server.jx3box.com/user/meta

params_key|value_type|ex
---|---|---
uid | int | 8
key | varchar | jx3_servers 

全部meta_key说明见[用户附表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_usermeta.md)

### Response Schema
#### 成功 200
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

#### 失败 400
自行根据response区分网络异常与返回异常
```json
{
    "msg": "非法请求",
    "code": 9999
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

全部meta_key说明见[用户附表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_usermeta.md)

### Response Schema
#### 成功 200
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

#### 失败 400
自行根据response区分网络异常与返回异常
```json
{
    "msg": "用户字段修改失败",
    "code": 10051,
    "data": {
        "uid": "8",
        "key": "jx3_servers",
        "value": "晴昼海"
    }
}
```