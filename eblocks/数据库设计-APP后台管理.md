## APP后台管理数据库表

### 消息通知 t_app_message


| 列名 | 类型 | 长度 | 是否主键 | 是否索引 |  是否为空 |  备注 |
| --- | --- | --- | --- | --- | --- | --- |
| id | bigint | 20 | 是 | 是 | 否 | 自增主键 |
| title | varchar | 64 | 否 | 否 | 否 | 标题 |
| content | text  | 1024 | 否 | 否 | 否 | 内容 |
| stu_course_ids | varchar  | 1024 | 否 | 否 | 是 | 接受课程级别信息 0:全部课程 |
| stu_class_ids | varchar  | 1024 | 否 | 否 | 是 | 接收班级信息 0:全部班级 |
| stu_ids | varchar  | 1024 | 否 | 否 | 是 | 接收学员信息 0:全部学员 |
| status | tinyint  | 10 | 否 | 否 | 否 | 状态 0:正常 |
| is_delete | bit  | 1 | 否 | 否 | 否 | 是否删除 0:正常 1:删除 默认0 |
| create_user_id | bigint | 64 | 否 | 否 | 否 | 创建人 |
| create_time | datetime | 0 | 否 | 否 | 否 | 创建时间 |
| last_modify_user_id | bigint | 64 | 否 | 否 | 否 | 最后修改人 |
| last_modify_time | datetime | 0 | 否 | 否 | 否 | 最后修改时间 |


### 消息通知记录 t_app_message_log


| 列名 | 类型 | 长度 | 是否主键 | 是否索引 |  是否为空 |  备注 |
| --- | --- | --- | --- | --- | --- | --- |
| id | bigint | 20 | 是 | 是 | 否 | 自增主键 |
| msg_id | bigint | 20 | 否 | 是 | 否 | 消息ID |
| stu_id | bigint | 20 | 否 | 是 | 否 | 学员用户ID |
| stu_number | varchar | 20 | 否 | 是 | 否 | 学员编号 |
| status | tinyint  | 10 | 否 | 否 | 否 | 状态 0:未读 1:已读 |
| read_time | datetime | 0 | 否 | 否 | 是 | 读取时间 |

