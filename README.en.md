[简体中文](README.md) | [繁體中文](README.zh-TW.md) | [English](README.en.md)

# Texas Hold'em Points Lobby Source Code - C++ Server and Tournament System

[![C++](https://img.shields.io/badge/server-C%2B%2B-00599c?logo=cplusplus)](./MatchServer.cpp)
[![Tars](https://img.shields.io/badge/protocol-Tars-1f6feb)](./MatchProto.tars)
[![License](https://img.shields.io/badge/license-see%20License.md-blue)](./License.md)

Source code for a Texas Hold'em points lobby, coin lobby, and multiplayer tournament system. The public repository primarily contains a **C++ / Tars match server**, including matchmaking, room messaging, game lifecycle handling, timers, order interfaces, reward configuration, and Classic Hold'em and Short Deck configuration.

> The repository contains Unity `Packages/` and `ProjectSettings/`, but not a complete Unity `Assets/` directory. The public files alone therefore do not constitute a buildable full client. See [PUBLIC-SCOPE.md](PUBLIC-SCOPE.md) and [License.md](License.md) for scope and licensing.

## Use Cases

- Server-side reference for poker points lobbies, coin lobbies, and clubs
- SNG and MTT matchmaking and room-flow implementation
- Classic Hold'em, 6+ Short Deck, insurance, and reward configuration
- C++ multiplayer server and Tars interface design

## Public Modules

| Area | Repository content |
| --- | --- |
| Matchmaking | `MatchServer.*`, `MatchServantImp.*`, `MatchServant.tars` |
| Protocols | `MatchProto.tars`, `OrderServant.tars`, room and client message headers |
| Game flow | Start, settlement, leave-table, timer, and dealing handlers |
| Configuration | Classic Hold'em, Short Deck, club, blind, and insurance structures |
| Rewards and orders | Tournament reward configuration and order service interfaces |

## Screenshots

| Points lobby | SNG tournament | Multi-table tournament |
| --- | --- | --- |
| ![Texas Hold'em points lobby](Screenshots/大厅01.png) | ![Texas Hold'em SNG tournament](Screenshots/sng05.jpg) | ![Texas Hold'em multi-table tournament](Screenshots/多座竞标赛1.jpg) |

Read the [English project page](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/en/) for the illustrated overview.

## Documentation and Contact

- [Public scope](PUBLIC-SCOPE.md)
- [Tournament server architecture](docs/server-architecture.md)
- [Matchmaking and game flow](docs/match-game-flow.md)
- [Tars protocols and messages](docs/tars-message-guide.md)
- Telegram: `@xuzongbin001`
- Email: `masterai918@gmail.com`

Comply with all applicable laws and platform rules. This repository does not encourage or support unlawful gambling.
