[简体中文](README.md) | [繁體中文](README.zh-TW.md) | [English](README.en.md)

# Texas Hold'em Points Lobby Source Code - C++/Tars Tournament Server

[![C++](https://img.shields.io/badge/server-C%2B%2B-00599c?logo=cplusplus)](MatchServer.cpp)
[![Tars](https://img.shields.io/badge/protocol-Tars-1f6feb)](MatchProto.tars)
[![Pages](https://img.shields.io/badge/demo-GitHub%20Pages-176b52)](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/en/)
[![License](https://img.shields.io/badge/license-see%20License.md-blue)](License.md)

This repository covers a **Texas Hold'em points lobby, coin lobby, and multiplayer tournament server**. Its public implementation is centered on C++ and Tars, with match information, player registration and state reporting, room messages, game lifecycle handlers, blind levels, rewards, order interfaces, Classic Hold'em, 6+ Short Deck, and insurance-related configuration.

Teams evaluating poker lobby source code, SNG/MTT services, or a C++ multiplayer game server can use the repository to inspect concrete protocols, handlers, configurations, and product screens before planning integration work.

> The repository includes Unity `Packages/` and `ProjectSettings/`,  Unity `Assets/` . Review [PUBLIC-SCOPE.md](PUBLIC-SCOPE.md), the [build guide](docs/build-guide.md), dependencies, and licensing first.

## Product Screens

| Points lobby | SNG tournament |
| --- | --- |
| ![Texas Hold'em points lobby source code game-mode screen](Screenshots/大厅01.png) | ![Texas Hold'em SNG tournament interface](Screenshots/sng05.jpg) |
| Multi-table tournament | Nine-player table |
| ![Texas Hold'em MTT multi-table tournament interface](Screenshots/多座竞标赛1.jpg) | ![Texas Hold'em nine-player multiplayer table](docs/Assets/screenshots/06-9.jpg) |

Explore the illustrated [English product page](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/en/) or switch to [Simplified Chinese](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-cn/) and [Traditional Chinese](https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/zh-tw/).

## Repository-backed Components

| Area | Primary files | Public implementation |
| --- | --- | --- |
| Match service | `MatchServer.*`, `MatchServantImp.*` | Service startup, configuration reload, match cleanup, and request handling |
| Tars contracts | `MatchProto.tars`, `MatchServant.tars` | Match, player, registration, quit, reward, and state structures |
| Game flow | `Processor.*`, `gamebegin.h`, `gameend.h` | Start, deal, settlement, leave-table, and room-message handling |
| Timers | `TimerThread.*`, `begintimer.*` | Match-start checks and timing logic |
| Order service | `OrderServant.tars`, `OrderServer.*` | Order contracts and service entry points |
| Game configuration | `config/gameconfig.*` | Blinds, Classic Hold'em, Short Deck, and insurance odds |
| Tournament rewards | `match_reward_config_*` | Reward query and update handlers |

## Evaluation Use Cases

- Architecture review for a points lobby or coin lobby server
- SNG and MTT registration, match state, ranking, and reward workflows
- Classic Hold'em, 6+ Short Deck, blind, and insurance configuration
- C++ multiplayer services, Tars IDL, and room-message design
- Technical validation before connecting proprietary account, payment, or operations systems

## Repository Map

```text
MatchServer.*             Match service entry point
MatchServantImp.*         Tars request implementation
MatchProto.tars           Match, registration, reward, and ranking contracts
Processor.*               Game and message processing
config/                   Game and service configuration
Screenshots/              README product screens
docs/                     GitHub Pages and technical documentation
Packages/                 Unity package configuration
ProjectSettings/          Unity project settings
```

## Suggested Review Process

1. Read [PUBLIC-SCOPE.md](PUBLIC-SCOPE.md) and [License.md](License.md).
2. Confirm Makefile, Tars, Linux, GCC/G++, and external dependency versions.
3. Start with protocol structures, service initialization, and configuration loading.
4. Validate registration, state changes, timers, rewards, and failure recovery in an isolated environment.
5. Do not use the project in production until required client assets and business dependencies are supplied and tested.

## Documentation and Related Projects

- [Tournament server architecture](docs/server-architecture.md)
- [Matchmaking and game flow](docs/match-game-flow.md)
- [Tars protocols and messages](docs/tars-message-guide.md)
- [Build and Unity completeness check](docs/build-guide.md)
- [Complete Texas Hold'em solution](https://github.com/masterai-top/TexasHoldem-Poker-Complete-Solution)
- [Texas Hold'em club source](https://github.com/masterai-top/TexasHoldem-Club-Source)
- [CFR poker AI source code](https://github.com/masterai-top/cfr-poker-ai-masterai)

## Contact and Responsible Use

Telegram: `@xuzongbin001` · Email: `masterai918@gmail.com`

Use this repository only for lawful software development, research, and technical evaluation. Follow applicable law, platform rules, privacy requirements, and protections for minors.
