[简体中文](README.md) | [繁體中文](README.zh-TW.md) | [English](README.en.md)

# 德州扑克积分大厅源码 - 金币大厅与 C++/Tars 多人赛事服务端

[![C++](https://img.shields.io/badge/server-C%2B%2B-00599c?logo=cplusplus)](MatchServer.cpp)
[![Tars](https://img.shields.io/badge/protocol-Tars-1f6feb)](MatchProto.tars)
[![Pages](https://img.shields.io/badge/demo-GitHub%20Pages-176b52)](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-cn/)
[![License](https://img.shields.io/badge/license-see%20License.md-blue)](License.md)

这是一个面向**德州扑克积分大厅、金币大厅和多人赛事**的源码项目。公开仓库以 C++/Tars 比赛服务端为主，包含比赛信息、用户报名、玩家状态、匹配与房间消息、牌局生命周期、盲注、奖励、订单、经典德州、6+短牌和保险相关配置。

如果你正在评估德州扑克大厅源码、SNG/MTT 赛事服务或 C++ 多人游戏服务器，本页面可以帮助你先从实际代码和界面确认项目范围，再决定如何测试与二次开发。

> 仓库包含 Unity 的 `Packages/` 与 `ProjectSettings/`， Unity `Assets/` 目录。请结合 [公开范围](PUBLIC-SCOPE.md)、[构建指南](docs/build-guide.md) 和实际验收结果进行评估。

## 产品界面

| 德州扑克积分大厅 | SNG 锦标赛 |
| --- | --- |
| ![德州扑克积分大厅源码大厅和游戏模式入口](Screenshots/大厅01.png) | ![德州扑克 SNG 单桌锦标赛界面](Screenshots/sng05.jpg) |
| 多桌锦标赛 | 九人桌牌局 |
| ![德州扑克 MTT 多桌锦标赛赛事界面](Screenshots/多座竞标赛1.jpg) | ![德州扑克九人桌多人牌局界面](docs/Assets/screenshots/06-9.jpg) |

更多产品图文：[简体中文页面](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-cn/) · [繁體中文](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-tw/) · [English](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/en/)

## 可以从源码核查的能力

| 方向 | 主要文件 | 公开内容 |
| --- | --- | --- |
| 比赛服务 | `MatchServer.*`、`MatchServantImp.*` | 服务初始化、配置重载、比赛清理与请求处理 |
| Tars 协议 | `MatchProto.tars`、`MatchServant.tars` | 比赛、玩家、报名、退出、奖励和状态数据结构 |
| 牌局流程 | `Processor.*`、`gamebegin.h`、`gameend.h` | 开始、发牌、结算、离桌及房间消息处理 |
| 定时任务 | `TimerThread.*`、`begintimer.*` | 比赛开始检查与计时相关逻辑 |
| 订单接口 | `OrderServant.tars`、`OrderServer.*` | 订单服务协议与服务入口 |
| 玩法配置 | `config/gameconfig.*` | 盲注、经典德州、短牌和保险赔率配置 |
| 奖励配置 | `match_reward_config_*` | 比赛奖励查询和更新相关处理 |

## 适用场景

- 德州扑克积分大厅或金币大厅服务端架构评估
- SNG、MTT 报名、比赛状态、玩家排名与奖励流程研究
- 经典德州、6+短牌、盲注和保险配置的二次开发参考
- C++ 多人游戏服务、Tars IDL 与房间消息设计学习
- 将现有客户端与自有账号、支付、运营系统进行集成前的技术验证

## 项目结构

```text
MatchServer.*             比赛服务入口
MatchServantImp.*         Tars 请求实现
MatchProto.tars           比赛、报名、奖励与排名协议
Processor.*               牌局与消息处理
config/                   玩法和服务配置
Screenshots/              README 产品截图
docs/                     GitHub Pages 与技术文档
Packages/                 Unity 包配置
ProjectSettings/          Unity 项目设置
```

## 评估与运行建议

1. 阅读 [PUBLIC-SCOPE.md](PUBLIC-SCOPE.md) 和 [License.md](License.md)，确认公开范围与授权。
2. 检查 Makefile、Tars、Linux、GCC/G++ 及外部依赖版本。
3. 从协议结构、服务初始化和配置加载开始进行最小化验证。
4. 在隔离测试环境检查比赛报名、状态变化、计时、奖励和异常恢复。
5. 在补齐客户端资源和业务依赖前，不要直接用于生产环境。

## 技术文档

- [比赛服务端架构](docs/server-architecture.md)
- [匹配与牌局流程](docs/match-game-flow.md)
- [Tars 协议和消息](docs/tars-message-guide.md)
- [构建与 Unity 完整性检查](docs/build-guide.md)
- [安全与合规](docs/security-compliance.md)
- [常见问题](docs/faq.md)

## MasterAI 相关项目

- [德州扑克完整解决方案](https://github.com/masterai-top/TexasHoldem-Poker-Complete-Solution)
- [德州扑克俱乐部源码](https://github.com/masterai-top/TexasHoldem-Club-Source)
- [德州扑克赛事平台](https://github.com/masterai-top/Texas-Holdem-Poker-Tournament-Event-Platform)
- [CFR 德州扑克 AI 源码](https://github.com/masterai-top/cfr-poker-ai-masterai)

## 联系与合规

- Telegram：`@xuzongbin001`
- Email：`masterai918@gmail.com`

请遵守所在地法律、平台规则、隐私与未成年人保护要求。本仓库用于合法的软件开发、研究和技术评估，不鼓励或支持违法赌博用途。
