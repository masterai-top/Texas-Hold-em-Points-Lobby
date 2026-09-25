# 德州扑克积分大厅与金币大厅源码说明

本页解释 `Texas-Hold-em-Points-Lobby` 中可核查的德州扑克积分大厅、德州金币大厅和赛事服务端范围，帮助开发者快速判断代码是否符合大厅、房间和比赛匹配的二次开发需求。

## 大厅与房间流程

1. 玩家通过积分大厅或金币大厅进入房间及赛事入口。
2. `MatchServer`、`MatchServantImp` 承接比赛入口、匹配和房间服务。
3. `MatchProto.tars`、`MatchServant.tars` 定义请求、响应及房间消息。
4. `Processor` 与开始、计时、离桌、结算处理文件推进牌局生命周期。
5. 奖励配置与 `OrderServant.tars` 提供赛事奖励和订单交互接口。

## 已公开玩法和能力

- 经典德州与 6+ Short Deck 配置
- 积分房、俱乐部房间和多人牌桌结构
- SNG 单桌锦标赛与 MTT 多桌赛事流程
- 盲注、保险、奖励、订单及房间消息
- C++ 多人游戏服务与 Tars RPC 协议

## 真实产品截图

| 积分与金币大厅 | SNG 赛事 | 九人牌桌 |
| --- | --- | --- |
| ![德州扑克积分大厅和金币大厅源码界面](Assets/screenshots/dating.jpg) | ![德州扑克 SNG 赛事源码界面](Assets/screenshots/sng.jpg) | ![德州扑克九人牌桌界面](Assets/screenshots/06-9.jpg) |

## 公开范围

仓库包含 Unity `Packages/` 和 `ProjectSettings/`，但没有完整 Unity `Assets/` 客户端目录。公开代码重点是 C++/Tars 服务端，不应据此宣称拥有未公开的完整客户端或运营后台。详见 [PUBLIC-SCOPE.md](../PUBLIC-SCOPE.md)。

相关入口：[项目 README](../README.md) · [服务端架构](server-architecture.md) · [匹配与牌局流程](match-game-flow.md)
