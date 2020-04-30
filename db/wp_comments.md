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
