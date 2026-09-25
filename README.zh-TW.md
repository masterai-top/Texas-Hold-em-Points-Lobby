[简体中文](README.md) | [繁體中文](README.zh-TW.md) | [English](README.en.md)

# 德州撲克積分大廳 / 金幣大廳原始碼 - 德州比賽與賽事伺服器

[![C++](https://img.shields.io/badge/server-C%2B%2B-00599c?logo=cplusplus)](MatchServer.cpp)
[![Tars](https://img.shields.io/badge/RPC-Tars-1683fa)](MatchProto.tars)
[![Project Site](https://img.shields.io/badge/site-GitHub%20Pages-1f883d)](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-tw/)

這是一個聚焦**德州撲克積分大廳原始碼、德州金幣大廳原始碼、德州比賽與德州賽事**的專案。公開倉庫以 **C++/Tars 多人比賽伺服器**為主，包含比賽配對、房間訊息、牌局生命週期、計時、訂單介面、獎勵設定，以及經典德州與 6+ 短牌相關結構。

倉庫可見 Unity `Packages/` 與 `ProjectSettings/`，但不含完整 Unity `Assets/` 客戶端目錄；公開範圍請以 [PUBLIC-SCOPE.md](PUBLIC-SCOPE.md) 為準。

## 專案定位與功能

- 德州撲克積分大廳、金幣大廳與房間入口
- 積分房、俱樂部房間與多人牌桌
- SNG 單桌錦標賽與 MTT 多桌賽事流程
- 經典德州與 6+ Short Deck 設定
- 盲注、保險、獎勵、訂單及房間訊息
- C++ 多人遊戲服務與 Tars RPC 介面

“德州比賽 / 德州賽事”在本倉庫中主要對應 SNG、MTT、比賽配對、房間訊息與獎勵設定，不代表倉庫包含未公開的賽事營運後台。

## 玩法與技術架構

| 模組 | 公開內容 | 主要檔案 |
| --- | --- | --- |
| 比賽與配對 | 比賽入口、配對、房間服務 | `MatchServer.*`、`MatchServantImp.*` |
| 通訊協議 | 請求、回應及房間訊息 | `MatchProto.tars`、`MatchServant.tars` |
| 牌局流程 | 開始、計時、離桌及結算 | `Processor.*` 與相關處理檔案 |
| 玩法設定 | 經典德州、短牌、盲注及保險 | `config/gameconfig.*` |
| 賽事與訂單 | SNG/MTT 獎勵及訂單介面 | 獎勵設定、`OrderServant.tars` |
| Unity 設定 | 套件與專案版本設定 | `Packages/`、`ProjectSettings/` |

## 真實產品畫面

下列圖片沿用線上 README 已展示的三類真實產品畫面，不新增不存在的後台或客戶端圖片。

| 積分與金幣大廳 | SNG 賽事 | 九人牌桌 |
| --- | --- | --- |
| ![德州撲克積分大廳與金幣大廳畫面](docs/Assets/screenshots/dating.jpg) | ![德州比賽與德州撲克 SNG 單桌賽事畫面](docs/Assets/screenshots/sng.jpg) | ![德州撲克九人桌遊戲畫面](docs/Assets/screenshots/06-9.jpg) |

完整圖文介紹：[繁體中文頁面](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-tw/)

## 文件與二次開發

- [德州撲克積分大廳與金幣大廳原始碼說明](docs/points-and-coin-lobby.md)
- [德州比賽與德州賽事伺服器說明](docs/texas-holdem-tournament.md)
- [比賽伺服器架構](docs/server-architecture.md)
- [配對與牌局流程](docs/match-game-flow.md)
- [Tars 協議與訊息](docs/tars-message-guide.md)
- [公開範圍與限制](PUBLIC-SCOPE.md)

建置前請確認 Linux、GCC/G++、Tars、依賴與脫敏設定版本。此倉庫不是可直接上線的完整客戶端，投入生產前仍需建置測試、安全審核、客戶端整合與法律合規評估。

## 聯絡與合規

- Telegram：[@xuzongbin001](https://t.me/xuzongbin001)
- Email：[masterai918@gmail.com](mailto:masterai918@gmail.com)

請遵守所在地法律、平台規則與授權要求。本倉庫不鼓勵或支援違法賭博用途。
