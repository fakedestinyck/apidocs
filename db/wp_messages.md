## 消息表

字段 | 类型 | 说明
---|---|---
ID | bigint | 消息ID
user_id | bigint | 用户ID
type | varchar(20) | 消息种类（如："cj","comment")
subtype | varchar(20) | 消息类型（如："post_reject"、"comment_post","comment_cmt"）
content | text | 消息正文
read | tinyint | 是否已读。0：未读  1：已读
created | int | 创建时间戳
updated | int | 更新时间戳
deleted | tinyint | 是否删除。0：未删除  1：已删除

## 评论消息
**type** : *comment*  
**subtype** : 
+ *comment_post* 文章评论
+ *comment_cmt* 评论回复