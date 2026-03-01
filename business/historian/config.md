# 史料官 Agent 配置

## 定期任务配置

### 创业日志更新 (每周)
```json
{
  "name": "史料官周报",
  "schedule": {"kind": "cron", "expr": "0 10 * * 6"},
  "payload": {"kind": "agentTurn", "message": "请执行：1. 从COO处获取本周业务动态 2. 撰写周度创业日志 3. 更新Notion创业日志页面 4. 生成社交媒体内容素材"},
  "sessionTarget": "isolated"
}
```

### 月度里程碑 (每月1号)
```json
{
  "name": "史料官月报",
  "schedule": {"kind": "cron", "expr": "0 10 1 * *"},
  "payload": {"kind": "agentTurn", "message": "请执行：1. 整理本月重要里程碑 2. 撰写月度故事 3. 更新Notion页面 4. 准备公众号/小红书内容"},
  "sessionTarget": "isolated"
}
```

## Notion API 配置
- Token: (请在环境变量中设置 NOTION_TOKEN)
- 创业日志页面: 3163bad3c1e281609892e781a4a73f1d
- 公司母页面: 3163bad3c1e280e587c0ec9374ec2bcd
