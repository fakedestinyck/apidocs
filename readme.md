# Developer Documents

## 全局设定
1. [详细说明](https://github.com/JX3BOX/apidocs/blob/master/global.md) 
2. [公用JSON](https://github.com/JX3BOX/jx3box-common/blob/master/js/jx3box.json)

## 数据表

主题|表名|说明|
---|---|---
用户 | [用户信息表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_users.md) | 账号与资料等
用户 | [用户字段表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_usermeta.md) | 用户扩展字段
文章 | [文章主表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_posts.md) | 文章ID/模式等
文章 | [文章扩展表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_postmeta.md) | 文章内容及meta
文章 | [文章设置表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_postsettings.md) | 高亮/统计等 (管理)
评论 | [评论主表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_comments.md) | 文章评论
消息 | [消息主表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_messages.md) | 站内消息内容
消息 | [消息字段表](https://github.com/JX3BOX/apidocs/blob/master/db/wp_message_metas.md) | 消息附属字符


## Token鉴权相关
名称|说明
---|---
[鉴权说明](https://github.com/JX3BOX/apidocs/blob/master/auth.md) | cookie + localstorage


## 后端API
名称|说明|域|开发人员|  
---|---|---|---|
[User](https://github.com/JX3BOX/apidocs/blob/master/api/account.md)|用户基础信息接口|server.jx3box.com|浮烟
[Usermeta](https://github.com/JX3BOX/apidocs/blob/master/api/usermeta.md)|用户扩展信息接口|server.jx3box.com|浮烟
[OAuth](https://github.com/JX3BOX/apidocs/blob/master/api/oauth.md) | 提供给第三方应用或跨项目账号登录|server.jx3box.com|浮烟
Extend|---|---|---|
[Api](https://github.com/JX3BOX/jx3box-api/blob/master/README.md)|评论/订阅/关注接口|api.jx3box.com|老胡
[Message](https://github.com/JX3BOX/apidocs/blob/master/api/message.md)|消息通知|helper.jx3box.com |苦瓜
os |中台| helper.jx3box.com | 苦瓜
-- |成就| helper.jx3box.com | 苦瓜
App|---|---|---|
[Spider](https://github.com/JX3BOX/apidocs/blob/master/api/spider.md)|边缘应用服务接口|spider.jx3box.com|浮烟
[Node](https://github.com/JX3BOX/apidocs/blob/master/api/node.md)|核心应用服务接口|node.jx3box.com|浮烟
[Hub](https://github.com/JX3BOX/jx3box-api/blob/master/README.md)|仓库服务接口|hub.jx3box.com|老胡

## 前端API
名称|说明|开发人员
---|---|---
[用户缓存信息](https://github.com/JX3BOX/apidocs/blob/master/api/user.md) | 通过localstorage调用本地缓存的用户信息 | 浮烟
[内容缓存数据库](https://github.com/JX3BOX/apidocs/blob/master/api/idb.md) | 通过IndexedDB调用历史分析或存储数据 | 浮烟
