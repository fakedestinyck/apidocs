# 评论表

字段 | 类型 | 说明
---|---|---
comment_ID | bigint | 评论ID
comment_post_ID | bigint | 评论所属文章ID
comment_parent | bigint | 回复的目标评论ID(评论给文章时为0)
user_id | bigint | 评论人ID
comment_author | varchar | 评论人
comment_date | datetime | 评论日期
comment_content | text | 评论内容
delete_user_id | uint64 | 删除该评论的用户
delete_at | uint64 |删除该评论的时间
status | int | 该评论的状态,0:正常评论, 1:未过审, 2:已删除
has_reply | tinyint | 1有0无