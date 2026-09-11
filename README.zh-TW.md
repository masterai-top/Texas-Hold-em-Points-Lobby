[简体中文](README.md) | [繁體中文](README.zh-TW.md) | [English](README.en.md)

# 德州撲克積分大廳原始碼（金幣大廳）- C++ 伺服器與多人賽事系統

[![C++](https://img.shields.io/badge/server-C%2B%2B-00599c?logo=cplusplus)](./MatchServer.cpp)
[![Tars](https://img.shields.io/badge/protocol-Tars-1f6feb)](./MatchProto.tars)
[![License](https://img.shields.io/badge/license-see%20License.md-blue)](./License.md)

這是一個面向德州撲克積分大廳、金幣大廳與多人賽事的原始碼倉庫。目前公開內容以 **C++ / Tars 比賽伺服器**為主，包含配對服務、房間訊息、牌局生命週期、計時器、訂單介面、獎勵設定，以及經典德州與短牌相關設定。

> 公開倉庫包含 Unity 的 `Packages/` 與 `ProjectSettings/`，但未包含完整 Unity `Assets/` 目錄，因此目前不能單憑這些檔案建置完整客戶端。實際授權範圍以 [PUBLIC-SCOPE.md](PUBLIC-SCOPE.md) 與 [License.md](License.md) 為準。

## 適用場景

- 德州撲克積分大廳、金幣大廳與俱樂部系統的伺服器研究
- SNG、MTT 錦標賽配對及房間流程參考
- 經典德州、6+ 短牌、保險與獎勵設定的二次開發
- C++ 多人遊戲伺服器與 Tars 介面設計學習

## 已公開的核心模組

| 模組 | 倉庫內容 |
| --- | --- |
| 比賽與配對 | `MatchServer.*`、`MatchServantImp.*`、`MatchServant.tars` |
| 協議與訊息 | `MatchProto.tars`、`OrderServant.tars`、房間及客戶端訊息檔案 |
| 牌局流程 | 開始、結算、離桌、計時及發牌相關 C++ 檔案 |
| 玩法設定 | 經典德州、短牌、俱樂部、盲注與保險設定結構 |
| 獎勵與訂單 | 比賽獎勵設定、訂單服務介面及相關實作 |

## 專案畫面

| 積分大廳 | SNG 賽事 | 多桌錦標賽 |
| --- | --- | --- |
| ![德州撲克積分大廳畫面](Screenshots/大厅01.png) | ![德州撲克 SNG 賽事畫面](Screenshots/sng05.jpg) | ![德州撲克多桌錦標賽畫面](Screenshots/多座竞标赛1.jpg) |

完整圖文介紹：[繁體中文頁面](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-tw/)

## 文件與聯絡

- [公開範圍與限制](PUBLIC-SCOPE.md)
- [比賽伺服器架構](docs/server-architecture.md)
- [配對與牌局流程](docs/match-game-flow.md)
- [Tars 協議與訊息](docs/tars-message-guide.md)
- Telegram：`@xuzongbin001`
- Email：`masterai918@gmail.com`

請遵守所在地法律與平台合規要求。本倉庫不鼓勵或支援任何違法賭博用途。
