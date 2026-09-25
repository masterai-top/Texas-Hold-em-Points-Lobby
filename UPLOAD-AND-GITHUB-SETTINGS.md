# 上传文件与 GitHub 设置

## 一、直接覆盖的文件

- `README.md`
- `README.zh-TW.md`
- `docs/zh-cn/index.html`
- `docs/zh-tw/index.html`

## 二、新增上传的文件

- `docs/points-and-coin-lobby.md`
- `docs/texas-holdem-tournament.md`
- `SEO-RANKING-REPORT.md`
- `UPLOAD-AND-GITHUB-SETTINGS.md`

其他源码、截图和配置文件保持原样。README 只引用线上原本已展示的 `dating.jpg`、`sng.jpg`、`06-9.jpg` 三类截图。

## 三、About 建议文案

在仓库右侧 About 的齿轮中填写：

```text
德州扑克积分大厅、金币大厅、德州比赛与赛事源码：C++/Tars、俱乐部、短牌、SNG、MTT。德州撲克賽事原始碼。
```

Website 保持：

```text
https://masterai-top.github.io/Texas-Hold-em-Points-Lobby/
```

## 四、Topics 建议

GitHub Topics 不支持中文，建议使用以下 20 个真实且不重复的英文主题：

```text
texas-holdem
texas-holdem-poker
poker
poker-game
poker-lobby
coin-lobby
points-lobby
poker-source-code
poker-server
game-server
multiplayer-game
online-poker
poker-club
short-deck-poker
sng
mtt
tars
cpp
unity
tournament-poker
```

删除重复或意图相近的旧词：`game-servers`、`texas-hold-em-poker`、`texas-holdem-poker-code`。`friend-game` 与当前主搜索意图较弱，也建议移除。

## 五、推荐上传顺序

1. 先覆盖两个 README 并上传两个专题 Markdown 文件。
2. 再覆盖 `docs/zh-cn/index.html` 和 `docs/zh-tw/index.html`，确认 GitHub Pages 构建成功。
3. 修改 About、Website 和 Topics。
4. 为本次文档改动创建一个清晰提交，例如：`Improve points lobby and tournament documentation`。
5. 在 Google Search Console 和 Bing Webmaster Tools 只提交 Pages 根页、简体页、繁体页及现有 `sitemap.xml`。

## 六、不建议操作

- 不建议修改仓库名；现有 URL 已被 Bing 收录，改名会增加迁移和索引风险。
- 不要把未公开的完整客户端、运营后台、数据库或一键部署写进 README。
- 不要新增与线上产品不一致的截图。
- 不要复制多份只有关键词不同的薄页面，搜索引擎可能将其视为重复内容。
- 不要承诺上传后立即前三；通常要观察 2-6 周，并结合真实外链、Stars、Release 和持续维护。
