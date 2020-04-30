# Account

## 基本信息 
### Request schema
***GET*** https://server.jx3box.com/user/info  

params_name|type|ex
---|---|--- 
uid | int | 8

### Response schema
```javascript
{
    msg: "用户信息获取成功",
    code: 10024,
    data: {
        uid: 8,
        name: "浮烟",
        avatar: "https://oss.jx3box.com/upload/avatar/682481.png",
        bio: "凭栏望千里，煮酒论江湖。",
        created_at: "2019-09-17T01:03:51.000Z",
    },
}
```
