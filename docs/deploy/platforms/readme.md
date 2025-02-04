# 消息平台说明

LangBot 需要连接消息平台 API 才能与用户交互，目前支持以下消息平台：


| 平台 | 状态 | 备注  |教程 |
| ------ | ---- | ---- | ---- |
| QQ 个人号 | ✅ | 使用普通的 QQ 号作为机器人，需要使用独立的协议端，支持 OneBot v11 和 go-cqhttp 协议 | [NapCat](/deploy/platforms/qq/aiocqhttp/napcat) <br> [Lagrange](/deploy/platforms/qq/aiocqhttp/lagrange) <br> [LiteLoaderQQNT](/deploy/platforms/qq/aiocqhttp/llonebot) <br> [Shamrock（不推荐）](/deploy/platforms/qq/aiocqhttp/shamrock) <br> [go-cqhttp（不推荐）](/deploy/platforms/qq/gocq) |
| QQ 官方机器人 | ✅ | 接入 QQ 开放平台的机器人 API | [教程](/deploy/platforms/qq/official) |
| 企业微信 | ✅ | 企业内部机器人 | [教程](/deploy/platforms/wecom/wecom) |
| 个人微信 | ✅ | 个人微信机器人 | [Gewechat](/deploy/platforms/wechat/gewechat) |
| 飞书 | ✅ |  | [教程](/deploy/platforms/lark) |
| Discord | ✅ |  | [教程](/deploy/platforms/discord) |