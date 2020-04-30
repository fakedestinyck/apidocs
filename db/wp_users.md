# 用户表
字段 | 类型 | 说明
---|---|---
ID | bigint | 用户ID
user_group | int | 用户组ID [释义详见](https://github.com/JX3BOX/apidocs/blob/master/global.md)
user_login | varchar | 用户名(默认注册为邮箱地址,第3方注册为非邮箱,当验证绑定邮箱后会更改为邮箱)
user_pass | varchar | 密码
display_name | varchar | 昵称
user_email | varchar | 绑定邮箱(用户未验证前,此字段不能作为发送邮箱依据,需以user_login字段为准)
verify_email | int | null或0为未验证,1为已验证
user_avatar | varchar | 头像原图地址,不能直接使用作为头像地址,需使用[user模块](https://github.com/JX3BOX/apidocs/blob/master/user.md)中`User.getInfo().avatar`方法获取,或自行使用Utils.showAvatar(原url,'s|m|l')作为最终显示.
user_bio | varchar | 用户签名
device_id | varchar | 设备UUID
github_id | int | github唯一ID
github_name | varchar | github用户名,可作为github链接地址关键词
qq_unionid | varchar | qq unionid,并未去除`UID_`前缀
qq_name | varchar | qq昵称
weibo_id | int | 微博UID,可作为微博链接地址关键字
weibo_name | varchar | 微博昵称
user_registered | datetime | 用户注册日期


