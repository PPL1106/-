# -
数据库层权限实现 3.1 创建 user_accessible_alerts 视图，自动过滤无权限记录 3.2 理解并使用 MySQL 的 CURRENT_USER () 函数 3.3 理解 DEFINER 与 INVOKER 的区别 3.4 使用视图的 WITH CHECK OPTION 约束 操作审计 4.1 独立部署只读 MySQL 实例专门存储审计日志 4.2 设计审计表记录：操作用户、操作类型、表名、记录 ID、IP 地址、User-Agent、时间戳 4.3 为 user_id 和 timestamp 添加复合索引支持快速查询 4.4 在 Flask 的 after_request 钩子中记录所有请求（排除健康检查等无关请求）
