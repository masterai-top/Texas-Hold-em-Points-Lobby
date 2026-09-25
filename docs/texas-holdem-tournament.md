# 德州比赛与德州赛事服务端说明

本页说明 `Texas-Hold-em-Points-Lobby` 中可核查的德州比赛、德州赛事、SNG 和 MTT 服务端范围，帮助开发者判断比赛匹配、房间消息、牌局流程和奖励配置是否符合二次开发需求。

## 德州比赛与赛事流程

1. 玩家从积分大厅或金币大厅选择 SNG、MTT 等赛事入口。
2. `MatchServer` 与 `MatchServantImp` 处理比赛入口、玩家匹配和房间服务。
3. `MatchProto.tars`、`MatchServant.tars` 定义赛事请求、响应和房间消息。
4. `Processor` 及开始、计时、离桌、结算相关文件推进牌局生命周期。
5. 比赛奖励配置和订单接口承接奖励及相关业务交互。

## 可核查的赛事模块

| 赛事能力 | 主要文件或结构 |
| --- | --- |
| 比赛服务入口 | `MatchServer.*` |
| 玩家匹配与房间实现 | `MatchServantImp.*` |
| 赛事及房间协议 | `MatchProto.tars`、`MatchServant.tars` |
| 牌局生命周期 | `Processor.*` 及开始、计时、离桌、结算文件 |
| SNG/MTT 奖励 | `match_reward_config_*` 文件 |
| 玩法和房间参数 | `config/gameconfig.*` |

## 真实赛事截图

| 积分与金币大厅 | SNG 德州比赛 | 九人牌桌 |
| --- | --- | --- |
| ![德州扑克积分大厅和赛事入口](Assets/screenshots/dating.jpg) | ![德州比赛与 SNG 德州扑克赛事界面](Assets/screenshots/sng.jpg) | ![德州扑克赛事九人牌桌](Assets/screenshots/06-9.jpg) |

公开仓库重点是 C++/Tars 服务端，不含完整 Unity `Assets/` 客户端目录，也不应宣称包含未公开的赛事运营后台。详见 [PUBLIC-SCOPE.md](../PUBLIC-SCOPE.md)。

相关入口：[项目 README](../README.md) · [积分大厅与金币大厅说明](points-and-coin-lobby.md) · [匹配与牌局流程](match-game-flow.md)
