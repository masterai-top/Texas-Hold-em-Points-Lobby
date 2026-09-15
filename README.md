[简体中文](README.md) | [繁體中文](README.zh-TW.md) | [English](README.en.md)

# 德州扑克积分大厅源码 - 金币大厅、积分房与 C++/Tars 赛事服务端

[![C++](https://img.shields.io/badge/server-C%2B%2B-00599c?logo=cplusplus)](MatchServer.cpp)
[![Tars](https://img.shields.io/badge/RPC-Tars-1683fa)](MatchProto.tars)
[![Project Site](https://img.shields.io/badge/site-GitHub%20Pages-1f883d)](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-cn/)

这是一个聚焦**德州扑克积分大厅源码、金币大厅、积分房和多人赛事服务端**的项目。公开仓库以 C++/Tars 服务端为主，包含比赛匹配、房间消息、牌局生命周期、计时处理、订单接口、奖励配置，以及经典德州和 6+ 短牌相关结构。

它与通用“德州扑克完整解决方案”不同：本仓库的重点是大厅入口、积分/金币房、俱乐部房间、SNG/MTT 流程及其服务端实现，便于开发团队评估匹配服务、牌局处理和二次开发范围。

> 仓库可见 Unity `Packages/` 与 `ProjectSettings/`

## 项目覆盖场景

- 德州扑克积分大厅与金币大厅
- 积分房、俱乐部房间和多人牌桌
- SNG 单桌锦标赛和 MTT 多桌赛事流程
- 经典德州与 6+ Short Deck 配置
- 盲注、保险、奖励、订单及房间消息
- C++ 多人游戏服务与 Tars RPC 接口

## 可核查的源码模块

| 模块 | 主要文件 | 用途 |
| --- | --- | --- |
| 匹配服务 | `MatchServer.*`、`MatchServantImp.*` | 比赛入口、匹配和服务实现 |
| Tars 协议 | `MatchProto.tars`、`MatchServant.tars` | 请求、响应和房间消息契约 |
| 牌局处理 | `Processor.*` 及开始、结算、离桌、计时文件 | 牌局生命周期与消息处理 |
| 订单服务 | `OrderServer.*`、`OrderServant.tars` | 订单接口及相关服务 |
| 游戏配置 | `config/gameconfig.*` | 经典德州、短牌、盲注、保险等参数 |
| 奖励配置 | 比赛奖励相关配置和实现 | SNG/MTT 奖励流程参考 |

## 真实产品界面

| 积分与金币大厅 | SNG 赛事 | 九人牌桌 |
| --- | --- | --- |
| ![德州扑克积分大厅和金币房源码界面](docs/Assets/screenshots/dating.jpg) | ![德州扑克 SNG 赛事源码界面](docs/Assets/screenshots/sng.jpg) | ![德州扑克九人桌游戏界面](docs/Assets/screenshots/06-9.jpg) |

更多图文说明：[简体中文](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-cn/) · [繁體中文](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-tw/) · [English](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/en/)

## 文档入口

- [比赛服务端架构](docs/server-architecture.md)
- [匹配与牌局流程](docs/match-game-flow.md)
- [Tars 协议与消息](docs/tars-message-guide.md)
- [构建检查](docs/build-guide.md)
- [安全与合规](docs/security-compliance.md)
- [常见问题](docs/faq.md)
- [公开范围](PUBLIC-SCOPE.md)

## 获取源码

```bash
git clone https://github.com/masterai-top/Texas-Hold-em-Points-Lobby.git
cd Texas-Hold-em-Points-Lobby
```

构建前请确认 Linux、GCC/G++、Tars、依赖库和脱敏配置版本。公开仓库不代表一键部署发行包，实际功能应以可复现构建和测试结果为准。

## 相关项目

- [德州扑克完整解决方案](https://github.com/masterai-top/TexasHoldem-Poker-Complete-Solution)
- [德州扑克赛事平台](https://github.com/masterai-top/Texas-Holdem-Poker-Tournament-Event-Platform)
- [CFR 德州扑克 AI](https://github.com/masterai-top/cfr-poker-ai-masterai)

## 联系与合规

- Telegram：[@xuzongbin001](https://t.me/xuzongbin001)
- Email：[masterai918@gmail.com](mailto:masterai918@gmail.com)

请遵守所在地法律法规、平台规则和许可证要求。本仓库不鼓励或支持违法赌博、结果操纵或未经授权的商业使用。
