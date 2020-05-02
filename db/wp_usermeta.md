# 用户扩展表

字段 | 类型 | 说明
---|---|---
umeta_id | bigint | ID
user_id | bigint | 用户ID
meta_key | varchar | 键名
meta_value | varchar | 键值

*user_id & meta_key 构成唯一索引*

## meta说明
键 | 描述 | 示例
---|---|---
jx3_servers | 开服监控·关注服务器列表 | "晴昼海,鹰击长空"
jx3price | 金价走势·关注的服务器 | "gate0101"
