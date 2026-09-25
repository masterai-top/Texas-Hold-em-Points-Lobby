[简体中文](README.md) | [繁體中文](README.zh-TW.md) | [English](README.en.md)

# 德州扑克积分大厅 / 金币大厅源码 - 德州比赛与赛事服务端

[![C++](https://img.shields.io/badge/server-C%2B%2B-00599c?logo=cplusplus)](MatchServer.cpp)
[![Tars](https://img.shields.io/badge/RPC-Tars-1683fa)](MatchProto.tars)
[![Project Site](https://img.shields.io/badge/site-GitHub%20Pages-1f883d)](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-cn/)

这是一个聚焦**德州扑克积分大厅源码、德州金币大厅源码、德州比赛和德州赛事**的项目。公开仓库以 **C++/Tars 多人比赛服务端**为主，包含比赛匹配、房间消息、牌局生命周期、计时处理、订单接口、奖励配置，以及经典德州和 6+ 短牌相关结构。

繁體關鍵詞：**德州撲克積分大廳原始碼、德州金幣大廳、德州比賽、德州賽事、德州撲克原始碼**。公开范围以仓库现有文件和 [PUBLIC-SCOPE.md](PUBLIC-SCOPE.md) 为准。

> 仓库可见 Unity `Packages/` 与 `ProjectSettings/`，但不含完整 Unity `Assets/` 客户端目录。请勿把公开文件误认为可直接上线的完整客户端。

## 目录

- [项目定位](#项目定位)
- [产品功能与大厅流程](#产品功能与大厅流程)
- [玩法与赛事](#玩法与赛事)
- [技术架构与源码入口](#技术架构与源码入口)
- [真实产品截图](#真实产品截图)
- [构建与二次开发](#构建与二次开发)
- [专题文档](#专题文档)
- [常见问题](#常见问题)

## 项目定位

本仓库面向积分大厅、金币大厅、俱乐部房间、SNG/MTT 和多人牌桌场景，便于开发团队评估匹配服务、牌局处理及二次开发范围。它与泛化的“德州扑克完整解决方案”不同：这里重点展示**大厅入口、积分/金币房和赛事服务端**。

- 德州扑克积分大厅、金币大厅和房间入口
- 积分房、俱乐部房间与多人牌桌
- SNG 单桌锦标赛和 MTT 多桌赛事流程
- 经典德州与 6+ Short Deck 配置
- 盲注、保险、奖励、订单及房间消息
- C++ 多人游戏服务与 Tars RPC 接口

## 产品功能与大厅流程

大厅负责承接玩家进入房间和赛事的入口；服务端通过匹配、房间消息和计时逻辑推进牌局。公开代码可核查以下流程：

1. 玩家从积分大厅或金币大厅选择房间及赛事入口。
2. `MatchServer` 和 `MatchServantImp` 处理比赛入口、匹配与房间服务。
3. `MatchProto.tars`、`MatchServant.tars` 定义请求、响应和房间消息。
4. `Processor` 及开始、离桌、计时、结算相关文件处理牌局生命周期。
5. 奖励配置和订单接口承接 SNG/MTT 奖励及相关业务交互。

“德州比赛 / 德州赛事”在本仓库中主要对应 SNG、MTT、比赛匹配、房间消息和奖励配置，不代表仓库包含未公开的赛事运营后台。

## 玩法与赛事

| 场景 | 公开内容 | 可核查入口 |
| --- | --- | --- |
| 经典德州 | 牌局、盲注、发牌、离桌和结算结构 | `Processor.*`、`config/gameconfig.*` |
| 6+ 短牌 | Short Deck 相关游戏配置 | `config/gameconfig.*` |
| SNG | 单桌比赛匹配、房间和奖励流程 | `MatchServantImp.*`、奖励配置文件 |
| MTT | 多人赛事服务、消息和奖励配置 | `MatchServer.*`、`MatchProto.tars` |
| 俱乐部房间 | 房间参数、消息与多人牌桌结构 | `onroommessage.h`、`MatchServant.tars` |
| 保险与订单 | 玩法参数和订单服务接口 | `config/gameconfig.*`、`OrderServant.tars` |

## 技术架构与源码入口

| 层级 | 主要文件 | 用途 |
| --- | --- | --- |
| 匹配服务 | `MatchServer.*`、`MatchServantImp.*` | 比赛入口、匹配和服务实现 |
| Tars 协议 | `MatchProto.tars`、`MatchServant.tars` | 请求、响应和房间消息契约 |
| 牌局处理 | `Processor.*` 及开始、结算、离桌、计时文件 | 牌局生命周期与消息处理 |
| 订单服务 | `OrderServer.*`、`OrderServant.tars` | 订单接口及相关服务 |
| 游戏配置 | `config/gameconfig.*` | 经典德州、短牌、盲注、保险等参数 |
| Unity 配置 | `Packages/`、`ProjectSettings/` | 包依赖及项目版本配置 |

## 真实产品截图

以下三类图片沿用本仓库线上 README 已展示的真实产品截图，不新增不存在的后台或客户端画面。

| 德州扑克积分与金币大厅 | SNG 赛事 | 九人牌桌 |
| --- | --- | --- |
| ![德州扑克积分大厅和金币大厅界面](docs/Assets/screenshots/dating.jpg) | ![德州比赛与德州扑克 SNG 单桌赛事界面](docs/Assets/screenshots/sng.jpg) | ![德州扑克九人桌游戏界面](docs/Assets/screenshots/06-9.jpg) |

更多图文说明：[简体中文](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-cn/) · [繁體中文](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-tw/) · [English](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/en/)

## 构建与二次开发

```bash
git clone https://github.com/masterai-top/Texas-Hold-em-Points-Lobby.git
cd Texas-Hold-em-Points-Lobby
```

构建前请确认 Linux、GCC/G++、Tars、依赖库和脱敏配置版本。公开仓库不代表一键部署发行包，实际功能应以可复现构建和测试结果为准。先阅读 [构建检查](docs/build-guide.md) 与 [公开范围](PUBLIC-SCOPE.md)。

## 专题文档

- [德州扑克积分大厅与金币大厅源码说明](docs/points-and-coin-lobby.md)
- [德州比赛与德州赛事服务端说明](docs/texas-holdem-tournament.md)
- [比赛服务端架构](docs/server-architecture.md)
- [匹配与牌局流程](docs/match-game-flow.md)
- [Tars 协议与消息](docs/tars-message-guide.md)
- [安全与合规](docs/security-compliance.md)
- [常见问题](docs/faq.md)

## 常见问题

### 这是完整的德州扑克客户端和运营后台吗？

不是。公开仓库的重点是 C++/Tars 服务端以及部分 Unity 配置，不应宣称包含未公开的完整客户端或运营后台。

### 积分大厅与金币大厅有什么区别？

它们是不同的大厅/房间业务入口。当前仓库公开了可用于评估匹配、房间、牌局、奖励和订单交互的服务端结构；具体资产规则应以部署配置和所在地合规要求为准。

### 是否可以直接上线？

不能未经检查直接投入生产。需要补齐依赖与配置，完成构建测试、安全审计、客户端集成和法律合规评估。

## 相关项目

- [德州扑克完整解决方案](https://github.com/masterai-top/TexasHoldem-Poker-Complete-Solution) - 承接“德州源码 / 德州扑克源码”等完整方案搜索意图
- [德州扑克赛事平台](https://github.com/masterai-top/Texas-Holdem-Poker-Tournament-Event-Platform)
- [CFR 德州扑克 AI](https://github.com/masterai-top/cfr-poker-ai-masterai)

## 联系与合规

- Telegram：[@xuzongbin001](https://t.me/xuzongbin001)
- Email：[masterai918@gmail.com](mailto:masterai918@gmail.com)

请遵守所在地法律法规、平台规则和许可证要求。本仓库不鼓励或支持违法赌博、结果操纵或未经授权的商业使用。
