# Developer Documents

## 全局设定
1. [详细说明](https://github.com/JX3BOX/apidocs/blob/master/global.md) 
2. [公用JSON](https://github.com/JX3BOX/jx3box-common/blob/master/js/jx3box.json)

## 数据表

主题|主表|附表|说明|
---|---|---|---
用户 | [用户主表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_users.md) | [用户附表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_usermeta.md) | 账号与资料等
文章 | [文章主表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_posts.md) | [文章附表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_postmeta.md) | 文章内容及meta
评论 | [评论主表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_comments.md) | [评论附表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_commentmeta.md) | 文章评论
消息 | [消息主表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_messages.md) | [消息附表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_message_metas.md) | 站内消息


## 前端API
MD|说明
---|---
[用户信息本地缓存](https://github.com/JX3BOX/apidocs/blob/master/api/user.md) | 通过localstorage调用本地缓存的用户信息(UID,头像,昵称等),减少不必要的请求
[第三方登录授权](https://github.com/JX3BOX/apidocs/blob/master/api/oauth.md) | 提供给第三方应用或跨项目账号登录


## 后端API
MD|说明
---|---
[用户接口](https://github.com/JX3BOX/apidocs/blob/master/api/account.md)|公开用户信息接口,获取头像等简要信息(无需鉴权)
[消息接口](https://github.com/JX3BOX/apidocs/blob/master/api/message.md)|PHP消息服务接口