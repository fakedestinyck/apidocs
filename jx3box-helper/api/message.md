## 目前还没有加上Token校验，TODO的都得改

### 创建用户消息（TODO）
POST /messages

##### 请求参数

参数 | 类型 | 必选 | 说明
---|---|---|---
user_id | int | 是 | 用户ID
type | string | 是 | 消息种类（如："cj")
subtype | string | 否 | 消息类型（如："post_reject"、"comment_checked"）
content | string | 是 | 消息内容
metas | array | 否 | 消息额外字段

##### 请求

```
{
    "user_id": 5,
    "type": "cj",
    "subtype": "post_reject",
    "content": "你的成就攻略被驳回",
    "metas": {
        "checker": "kuguats",
        "reason": "成就攻略恶意覆盖"
    }
}
```

##### 响应

```
# 成功
{
    "code": 200,
    "message": "消息创建成功",
    "data": {"id":233}
}

# 失败
{
    "code": 400,
    "message": "消息创建失败"
}
```

### 获取用户消息（TODO）
GET /messages

##### 请求参数

参数 | 类型 | 必选 | 说明
---|---|---|---
length | int | 否 | 最大返回条数（默认：10）
fields | array | 否 | 需要请求的字段
where | array | 否 | 筛选条件（目前只有"content"字段为模糊匹配）

##### 请求

```
{
    "length": 10,
    "fields": ["checker","reason"],
    "where": {
        "checker": "kuguats"
    }
}
```

##### 响应

```
# 成功
{
    "code": 200,
    "message": "消息列表",
    "data": {
        "messages": [
            {
                "id": 232, 
                "type": "fb", 
                "subtype": "checked",
                "metas": {
                    "checker": "kuguats", 
                    "reason": null
                }, 
                // ...等基本字段
            },
            {
                "id": 233, 
                "type": "cj", 
                "subtype": "post_reject",
                "metas": {
                    "checker": "kuguats", 
                    "reason": "成就攻略恶意覆盖"
                }, 
                // ...等基本字段
            }
        ],
        "unread_count": 1
    }
}

# 失败
{
    "code": 400,
    "message": "字段fields类型必须为数组"
}
```

### 设置消息为已读（TODO）
PUT /messages/read

##### 请求参数

参数 | 类型 | 必选 | 说明
---|---|---|---
user_id | int | 是 | 用户ID
ids | array | 是 | 消息ID数组

##### 请求

```
{
    "user_id": 5,
    "ids": [2, 23, 233]
}
```

##### 响应

```
# 成功
{
    "code": 200,
    "message": "消息更新成功",
    "data": {
        "updated": 3 // 更新条数
    }
}

# 失败
{
    "code": 400,
    "message": "消息更新失败"
}
```