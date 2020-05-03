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


## Token鉴权相关
名称|说明
---|---
[本地测试鉴权配置](https://github.com/JX3BOX/apidocs/blob/master/auth.md) | 本地环境测试线上接口
[跨主域本地用户信息](https://github.com/JX3BOX/apidocs/blob/master/api/user.md) | 通过localstorage调用本地缓存的用户信息(UID,头像,昵称等),减少不必要的请求


## API
名称|说明|域|开发人员|
---|---|---|---|
[User](https://github.com/JX3BOX/apidocs/blob/master/api/account.md)|用户基础信息接口|server.jx3box.com|浮烟
[Usermeta](https://github.com/JX3BOX/apidocs/blob/master/api/usermeta.md)|用户扩展信息接口|server.jx3box.com|浮烟
[OAuth](https://github.com/JX3BOX/apidocs/blob/master/api/oauth.md) | 提供给第三方应用或跨项目账号登录|server.jx3box.com|浮烟
---|---|---|---|
[Message](https://github.com/JX3BOX/apidocs/blob/master/api/message.md)|消息通知|helper.jx3box.com |苦瓜
-- |成就| helper.jx3box.com | 苦瓜
os |中台| helper.jx3box.com | 苦瓜
[Spider](https://github.com/JX3BOX/apidocs/blob/master/api/spider.md)|边缘应用服务接口|spider.jx3box.com|浮烟
[Node](https://github.com/JX3BOX/apidocs/blob/master/api/node.md)|核心应用服务接口|node.jx3box.com|浮烟

