[简体中文](README.md) | [繁體中文](README.zh-TW.md) | [English](README.en.md)

# 德州撲克積分大廳原始碼 - 金幣大廳與 C++/Tars 多人賽事伺服器

[![C++](https://img.shields.io/badge/server-C%2B%2B-00599c?logo=cplusplus)](MatchServer.cpp)
[![Tars](https://img.shields.io/badge/protocol-Tars-1f6feb)](MatchProto.tars)
[![Pages](https://img.shields.io/badge/demo-GitHub%20Pages-176b52)](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-tw/)
[![License](https://img.shields.io/badge/license-see%20License.md-blue)](License.md)

本專案聚焦**德州撲克積分大廳、金幣大廳及多人賽事**。公開儲存庫以 C++/Tars 比賽伺服器為核心，提供比賽資訊、使用者報名、玩家狀態、配對與房間訊息、牌局生命週期、盲注、獎勵、訂單、經典德州、6+短牌及保險相關設定。

對於正在比較德州撲克大廳原始碼、SNG/MTT 賽事服務或 C++ 多人遊戲伺服器的團隊，可先由實際程式碼、協議與產品畫面確認技術範圍，再規劃測試及二次開發。

> 儲存庫包含 Unity `Packages/` 與 `ProjectSettings/`， Unity `Assets/` 目錄。請先閱讀 [公開範圍](PUBLIC-SCOPE.md) 與 [建置指南](docs/build-guide.md)。

## 實際產品畫面

| 德州撲克積分大廳 | SNG 單桌賽 |
| --- | --- |
| ![德州撲克積分大廳原始碼遊戲入口](Screenshots/大厅01.png) | ![德州撲克 SNG 單桌錦標賽畫面](Screenshots/sng05.jpg) |
| MTT 多桌錦標賽 | 九人桌牌局 |
| ![德州撲克 MTT 多桌錦標賽畫面](Screenshots/多座竞标赛1.jpg) | ![德州撲克九人桌多人牌局畫面](docs/Assets/screenshots/06-9.jpg) |

更多圖文：[繁體中文產品頁](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-tw/) · [简体中文](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-cn/) · [English](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/en/)

## 可由儲存庫核對的模組

| 方向 | 主要檔案 | 公開內容 |
| --- | --- | --- |
| 比賽服務 | `MatchServer.*`、`MatchServantImp.*` | 服務初始化、設定重載、比賽清理及請求處理 |
| Tars 協議 | `MatchProto.tars`、`MatchServant.tars` | 比賽、玩家、報名、退出、獎勵與狀態結構 |
| 牌局流程 | `Processor.*`、`gamebegin.h`、`gameend.h` | 開始、發牌、結算、離桌與房間訊息 |
| 計時處理 | `TimerThread.*`、`begintimer.*` | 比賽開始檢查及計時邏輯 |
| 訂單服務 | `OrderServant.tars`、`OrderServer.*` | 訂單介面與服務入口 |
| 玩法設定 | `config/gameconfig.*` | 盲注、經典德州、短牌及保險賠率 |
| 賽事獎勵 | `match_reward_config_*` | 獎勵查詢與更新相關處理 |

## 適合的技術評估方向

- 積分大廳與金幣大廳的伺服器架構
- SNG、MTT 報名、比賽狀態、玩家排名與獎勵流程
- 經典德州、6+短牌、盲注與保險設定
- C++ 多人遊戲服務、Tars IDL 及房間訊息設計
- 與自有帳號、支付及營運系統整合前的可行性驗證

## 目錄導覽

```text
MatchServer.*             比賽服務入口
MatchServantImp.*         Tars 請求實作
MatchProto.tars           比賽、報名、獎勵與排名協議
Processor.*               牌局及訊息處理
config/                   玩法與服務設定
Screenshots/              README 產品畫面
docs/                     GitHub Pages 與技術文件
Packages/                 Unity 套件設定
ProjectSettings/          Unity 專案設定
```

## 文件與相關專案

- [比賽伺服器架構](docs/server-architecture.md)
- [配對與牌局流程](docs/match-game-flow.md)
- [Tars 協議與訊息](docs/tars-message-guide.md)
- [建置與 Unity 完整性檢查](docs/build-guide.md)
- [德州撲克完整解決方案](https://github.com/masterai-top/TexasHoldem-Poker-Complete-Solution)
- [德州撲克俱樂部原始碼](https://github.com/masterai-top/TexasHoldem-Club-Source)
- [CFR 德州撲克 AI](https://github.com/masterai-top/cfr-poker-ai-masterai)

## 聯絡與合規

Telegram：`@xuzongbin001` · Email：`masterai918@gmail.com`

請遵守所在地法律、平台規則、隱私及未成年人保護要求。本專案僅供合法軟體開發、研究和技術評估使用。
