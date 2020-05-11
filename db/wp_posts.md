# 文章表

字段 | 类型 | 说明
---|---|---
ID | bigint | 文章ID
post_author | bigint | 作者ID
post_date | datetime | 发布时间
post_modified | datetime | 更新时间
post_title | text | 文章标题
post_content | longtext | 文章内容
post_type | varchar | 文章类别 [释义详见](https://github.com/JX3BOX/apidocs/blob/master/global.md)
post_excerpt | text | 文章摘要
post_status | varchar | 文章状态 
post_mode | varchar | 编辑模式(tinymce|markdown) 

## post_status 文章发布状态
+ publish 已发布
+ dustbin 已删除
+ draft 草稿
+ pending 待审核
