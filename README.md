# MySQL权限控制与操作审计
## 项目背景
本项目是小组作业实现，核心完成「数据库层权限控制」和「操作行为审计」两大核心需求，适配MySQL 8.0 + Flask框架。

## 核心功能
### 1. 数据库层权限实现（3.1-3.4）
- 创建`user_accessible_alerts`视图，基于`CURRENT_USER()`动态过滤数据；
- 验证DEFINER/INVOKER权限差异；
- 视图添加`WITH CHECK OPTION`约束，防止越权修改数据。

### 2. 操作审计（4.1-4.4）
- 独立部署MySQL实例存储审计日志；
- 设计审计表记录操作人、IP、操作类型等关键信息；
- 为审计表添加复合索引提升查询效率；
- Flask钩子实现请求日志自动记录（排除健康检查）。

## 快速使用
### 1. 环境准备
- 安装MySQL 8.0（业务库+独立审计库）；
- 安装Python依赖：`pip install -r python/requirements.txt`。

### 2. 执行SQL脚本
按sql目录下的文件顺序执行，先建业务表，再建视图/审计表。

### 3. 运行Flask审计服务
```bash
cd python
python app.py
