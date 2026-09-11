[简体中文](README.md) | [繁體中文](README.zh-TW.md) | [English](README.en.md)

# 德州扑克积分大厅源码（德州金币大厅）- C++ 服务端与多人赛事系统

[![C++](https://img.shields.io/badge/server-C%2B%2B-00599c?logo=cplusplus)](./MatchServer.cpp)
[![Tars](https://img.shields.io/badge/protocol-Tars-1f6feb)](./MatchProto.tars)
[![License](https://img.shields.io/badge/license-see%20License.md-blue)](./License.md)

这是一个面向德州扑克积分大厅、金币大厅和多人赛事场景的源码仓库。当前公开内容以 **C++ / Tars 比赛服务端**为主，包含匹配服务、房间消息、牌局生命周期、计时器、订单接口、奖励配置，以及经典德州和短牌相关配置。

> 公开仓库包含 Unity 的 `Packages/` 与 `ProjectSettings/`，但未包含完整的 Unity `Assets/` 目录，因此不能仅凭当前文件构建完整客户端。实际交付与授权范围请以 [PUBLIC-SCOPE.md](PUBLIC-SCOPE.md) 和 [License.md](License.md) 为准。

## 适用场景

- 德州扑克积分大厅、金币大厅与俱乐部系统的服务端研究
- SNG、MTT 等锦标赛匹配和房间流程参考
- 经典德州、6+ 短牌、保险和奖励配置的二次开发
- C++ 多人游戏服务端与 Tars 接口设计学习

## 已公开的核心模块

| 模块 | 仓库中的对应内容 |
| --- | --- |
| 比赛与匹配 | `MatchServer.*`、`MatchServantImp.*`、`MatchServant.tars` |
| 协议与消息 | `MatchProto.tars`、`OrderServant.tars`、房间与客户端消息头文件 |
| 牌局流程 | 开始、结算、离桌、计时与发牌相关 C++ 文件 |
| 玩法配置 | 经典德州、短牌、俱乐部、盲注、保险等配置结构 |
| 奖励与订单 | 比赛奖励配置、订单服务接口与相关实现 |

## 项目截图

| 积分大厅 | SNG 赛事 | 多桌锦标赛 |
| --- | --- | --- |
| ![德州扑克积分大厅界面](Screenshots/大厅01.png) | ![德州扑克 SNG 赛事界面](Screenshots/sng05.jpg) | ![德州扑克多桌锦标赛界面](Screenshots/多座竞标赛1.jpg) |

更多图文页面：[简体中文](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-cn/) · [繁體中文](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-tw/) · [English](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/en/)

## 文档

- [公开范围与限制](PUBLIC-SCOPE.md)
- [比赛服务端架构](docs/server-architecture.md)
- [构建与 Unity 完整性检查](docs/build-guide.md)
- [匹配与牌局流程](docs/match-game-flow.md)
- [Tars 协议与消息](docs/tars-message-guide.md)
- [安全与合规](docs/security-compliance.md)
- [常见问题](docs/faq.md)

## 获取与检查

```bash
git clone https://github.com/masterai-top/Texas-Hold-em-Points-Lobby.git
cd Texas-Hold-em-Points-Lobby
```

构建前请先阅读 [构建指南](docs/build-guide.md)，并确认 Linux、GCC/G++、Tars、依赖库和配置文件版本。不要将测试环境直接用于生产环境。

## 相关项目

- [德州扑克完整解决方案](https://github.com/masterai-top/TexasHoldem-Poker-Complete-Solution)
- [德州扑克赛事平台](https://github.com/masterai-top/Texas-Holdem-Poker-Tournament-Event-Platform)
- [CFR 德州扑克 AI](https://github.com/masterai-top/cfr-poker-ai-masterai)

## 联系

- Telegram：`@xuzongbin001`
- Email：`masterai918@gmail.com`

请遵守所在地法律法规及平台合规要求。本仓库不鼓励或支持任何违法赌博用途。
