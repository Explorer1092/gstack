# gstack

你好，我是 [Garry Tan](https://x.com/garrytan)。我是 [Y Combinator](https://www.ycombinator.com/) 的总裁兼 CEO。在 YC，我与数千家初创公司合作过，包括 Coinbase、Instacart 和 Rippling——当时这些公司的创始人只有一两个人在车库里起步，如今市值已达数百亿美元。在加入 YC 之前，我设计了 Palantir 的 logo，并且是那里最早的工程经理/产品经理/设计师之一。我联合创立了 Posterous（一个博客平台，后被 Twitter 收购）。2013 年，我开发了 Bookface——YC 的内部社交网络。我作为设计师、产品经理和工程经理，已经做了很长时间的产品开发。

而现在，我正在经历一个全新时代的开端。

在过去的 60 天里，我编写了**超过 60 万行生产代码**——其中 35% 是测试代码——并且我每天能产出**10,000 到 20,000 行可用代码**，这只是我在担任 YC CEO 全部职责之余的兼职工作。这不是打错字。我最近一次 `/retro`（过去 7 天的开发统计，横跨 3 个项目）的数据是：**新增 140,751 行代码，362 次提交，净增约 115,000 行代码**。模型每周都在显著进步。我们正处于一个真实变革的黎明——一个人就能完成过去二十人团队的工作量。

**2026 年——1,237 次贡献，还在持续增长：**

![GitHub 贡献 2026——1,237 次贡献，1 至 3 月大幅增长](docs/images/github-2026.png)

**2013 年——我在 YC 开发 Bookface 时（772 次贡献）：**

![GitHub 贡献 2013——772 次贡献，在 YC 开发 Bookface](docs/images/github-2013.png)

同一个人，不同的时代。区别在于工具。

**gstack 就是我的秘诀。** 它是我的开源软件工厂。它将 Claude Code 变成一个你真正可以管理的虚拟工程团队——一个重新思考产品的 CEO、一个锁定架构的工程经理、一个捕捉 AI 瑕疵的设计师、一个寻找生产环境 bug 的偏执审查员、一个打开真实浏览器逐步测试你应用的 QA 负责人，以及一个提交 PR 的发布工程师。15 个专家角色和 6 个强力工具，全部以斜杠命令触发，全部基于 Markdown，**全部免费，MIT 许可证，现在就可以使用。**

我正在探索 2026 年 3 月 AI 智能体系统的能力边界，这是我的实时实验。我分享出来，是因为我希望全世界都与我同行。

Fork 它，改进它，让它成为你自己的。不要嫉妒，要欣赏。

**适用人群：**
- **创始人和 CEO** ——尤其是那些仍然想亲自写代码的技术型创始人。这就是你用一个人的力量完成二十人团队工作的方法。
- **Claude Code 新手** —— gstack 是最好的入门方式。结构化的角色，而不是空白的提示词。
- **技术负责人和高级工程师** ——为每个 PR 带来严格的代码审查、QA 和发布自动化。

## 快速开始：你的前 10 分钟

1. 安装 gstack（30 秒——见下文）
2. 运行 `/office-hours` ——描述你正在开发的东西。它会在你写一行代码之前重新定义问题。
3. 对任何功能想法运行 `/plan-ceo-review`
4. 对任何有变更的分支运行 `/review`
5. 对你的测试环境 URL 运行 `/qa`
6. 到这里就够了。你会知道这是否适合你。

第一次有效运行预计在 5 分钟内完成（前提是项目已有测试配置）。

**如果你只打算多看一个章节，就看这个。**

## 安装——只需 30 秒

**环境要求：** [Claude Code](https://docs.anthropic.com/en/docs/claude-code)、[Git](https://git-scm.com/)、[Bun](https://bun.sh/) v1.0+、[Node.js](https://nodejs.org/)（仅 Windows 需要）

### 第一步：安装到你的机器上

打开 Claude Code，粘贴以下内容。Claude 会完成剩下的工作。

> 安装 gstack：运行 **`git clone https://github.com/garrytan/gstack.git ~/.claude/skills/gstack && cd ~/.claude/skills/gstack && ./setup`**，然后在 CLAUDE.md 中添加一个 "gstack" 章节，说明使用 gstack 的 /browse 技能进行所有网页浏览，永远不要使用 mcp\_\_claude-in-chrome\_\_\* 工具，并列出可用的技能：/office-hours、/plan-ceo-review、/plan-eng-review、/plan-design-review、/design-consultation、/review、/ship、/browse、/qa、/qa-only、/design-review、/setup-browser-cookies、/retro、/investigate、/document-release、/codex、/careful、/freeze、/guard、/unfreeze、/gstack-upgrade。然后询问用户是否也想把 gstack 添加到当前项目中，以便团队成员也能使用。

### 第二步：添加到你的仓库中让团队成员也能使用（可选）

> 将 gstack 添加到此项目：运行 **`cp -Rf ~/.claude/skills/gstack .claude/skills/gstack && rm -rf .claude/skills/gstack/.git && cd .claude/skills/gstack && ./setup`**，然后在此项目的 CLAUDE.md 中添加一个 "gstack" 章节，说明使用 gstack 的 /browse 技能进行所有网页浏览，永远不要使用 mcp\_\_claude-in-chrome\_\_\* 工具，列出可用的技能：/office-hours、/plan-ceo-review、/plan-eng-review、/plan-design-review、/design-consultation、/review、/ship、/browse、/qa、/qa-only、/design-review、/setup-browser-cookies、/retro、/investigate、/document-release、/codex、/careful、/freeze、/guard、/unfreeze、/gstack-upgrade，并告诉 Claude 如果 gstack 技能无法正常工作，运行 `cd .claude/skills/gstack && ./setup` 来构建二进制文件并注册技能。

真实文件会提交到你的仓库中（不是 submodule），所以 `git clone` 就能直接使用。所有内容都在 `.claude/` 目录下，不会修改你的 PATH，也不会在后台运行任何东西。

### Codex、Gemini CLI 或 Cursor

gstack 可在任何支持 [SKILL.md 标准](https://github.com/anthropics/claude-code)的智能体上运行。技能位于 `.agents/skills/` 目录，会被自动发现。

```bash
git clone https://github.com/garrytan/gstack.git ~/.codex/skills/gstack
cd ~/.codex/skills/gstack && ./setup --host codex
```

或者让 setup 自动检测你安装了哪些智能体：

```bash
git clone https://github.com/garrytan/gstack.git ~/gstack
cd ~/gstack && ./setup --host auto
```

这会根据可用的工具安装到 `~/.claude/skills/gstack` 和/或 `~/.codex/skills/gstack`。全部 21 个技能在所有支持的智能体上都可使用。基于 hook 的安全技能（careful、freeze、guard）在非 Claude 宿主上使用内联安全提示。

## 看看它是怎么工作的

```
你：    我想做一个日历的每日简报应用。
你：    /office-hours
Claude：[询问具体痛点——要真实案例，不要假设]

你：    多个 Google 日历，活动信息过时，地点错误。
        准备工作花很长时间，结果还不够好……

Claude：我要挑战一下你的表述。你说的是"每日简报应用"。
        但你实际描述的是一个个人首席幕僚 AI。
        [提取出你自己都没意识到的 5 项能力]
        [挑战 4 个前提假设——你可以同意、反对或调整]
        [生成 3 种实现方案及工作量估算]
        建议：先发布最小可行版本，从真实使用中学习。
        完整愿景是一个 3 个月的项目——从一个真正好用的
        每日简报开始。
        [撰写设计文档 → 自动传递给下游技能]

你：    /plan-ceo-review
        [读取设计文档，挑战范围，运行 10 个维度的评审]

你：    /plan-eng-review
        [ASCII 数据流图、状态机、错误路径]
        [测试矩阵、故障模式、安全问题]

你：    批准计划。退出计划模式。
        [在 11 个文件中写入 2,400 行代码。约 8 分钟。]

你：    /review
        [自动修复] 2 个问题。[询问] 竞态条件 → 你批准修复。

你：    /qa https://staging.myapp.com
        [打开真实浏览器，逐步点击测试流程，发现并修复一个 bug]

你：    /ship
        测试：42 → 51（+9 新增）。PR：github.com/you/app/pull/42
```

你说"每日简报应用"。智能体说"你正在构建一个首席幕僚 AI"——因为它听的是你的痛点，而不是你的功能需求。然后它挑战了你的前提假设，生成了三种方案，推荐了最小可行版本，并撰写了一份设计文档，供每个下游技能读取。八个命令。这不是一个副驾驶，这是一个团队。

## 冲刺流程

gstack 是一套流程，而不是一堆工具的集合。技能的排列顺序遵循冲刺的运作方式：

**思考 → 规划 → 构建 → 审查 → 测试 → 发布 → 复盘**

每个技能都为下一个技能提供输入。`/office-hours` 撰写的设计文档由 `/plan-ceo-review` 读取。`/plan-eng-review` 撰写的测试计划由 `/qa` 获取。`/review` 发现的 bug 由 `/ship` 验证已修复。没有任何环节会被遗漏，因为每一步都知道之前发生了什么。

一次冲刺，一个人，一个功能——使用 gstack 大约需要 30 分钟。但真正改变一切的是：你可以同时并行运行 10-15 个冲刺。不同的功能、不同的分支、不同的智能体——全部同时进行。这就是我在做本职工作的同时，每天能产出 10,000 多行生产代码的原因。

| 技能 | 你的专家 | 功能描述 |
|------|---------|---------|
| `/office-hours` | **YC Office Hours** | 从这里开始。六个核心问题，在你写代码之前重新定义你的产品。挑战你的表述，质疑前提，生成替代方案。设计文档自动传递给所有下游技能。 |
| `/plan-ceo-review` | **CEO / 创始人** | 重新思考问题。找到隐藏在需求中的 10 星产品。四种模式：扩展、选择性扩展、保持范围、缩减。 |
| `/plan-eng-review` | **工程经理** | 锁定架构、数据流、图表、边界情况和测试。将隐藏的假设暴露出来。 |
| `/plan-design-review` | **高级设计师** | 对每个设计维度评分 0-10，解释 10 分是什么样子，然后修改计划以达到目标。AI 瑕疵检测。交互式——每个设计决策都会询问用户。 |
| `/design-consultation` | **设计合伙人** | 从零开始构建完整的设计系统。了解行业现状，提出安全选择和创意冒险，生成真实的产品样式。设计贯穿所有其他阶段。 |
| `/review` | **资深工程师** | 找到通过 CI 但在生产环境中爆炸的 bug。自动修复明显的问题，标记完整性缺陷。 |
| `/investigate` | **调试专家** | 系统化的根因调试。铁律：不调查清楚就不修复。追踪数据流、验证假设、3 次修复失败后停止。 |
| `/design-review` | **会写代码的设计师** | 与 /plan-design-review 相同的审计，然后修复发现的问题。原子提交，前后对比截图。 |
| `/qa` | **QA 负责人** | 测试你的应用，发现 bug，通过原子提交修复，重新验证。为每个修复自动生成回归测试。 |
| `/qa-only` | **QA 报告员** | 与 /qa 相同的方法论，但只生成报告。当你需要纯粹的 bug 报告而不需要代码修改时使用。 |
| `/ship` | **发布工程师** | 同步 main 分支，运行测试，审计覆盖率，推送，创建 PR。如果项目没有测试框架，会从零搭建。一个命令搞定。 |
| `/document-release` | **技术文档工程师** | 更新所有项目文档以匹配刚刚发布的内容。自动捕获过时的 README。 |
| `/retro` | **工程经理** | 团队感知的周复盘。按人分析、发布连续性、测试健康趋势、成长机会。 |
| `/browse` | **QA 工程师** | 赋予智能体"眼睛"。真正的 Chromium 浏览器、真实的点击、真实的截图。每条命令约 100 毫秒。 |
| `/setup-browser-cookies` | **会话管理员** | 从你的真实浏览器（Chrome、Arc、Brave、Edge）导入 cookies 到无头浏览器会话。测试需要登录的页面。 |

### 强力工具

| 技能 | 功能描述 |
|------|---------|
| `/codex` | **第二意见** ——来自 OpenAI Codex CLI 的独立代码审查。三种模式：审查（通过/失败门禁）、对抗性挑战、开放咨询。当 `/review` 和 `/codex` 都审查过同一分支时，提供跨模型分析。 |
| `/careful` | **安全护栏** ——在执行破坏性命令（rm -rf、DROP TABLE、force-push）前发出警告。说"小心点"即可激活。可覆盖任何警告。 |
| `/freeze` | **编辑锁定** ——将文件编辑限制在一个目录内。调试时防止意外修改范围外的代码。 |
| `/guard` | **全面安全** —— `/careful` + `/freeze` 合二为一。生产环境工作的最高安全级别。 |
| `/unfreeze` | **解锁** ——移除 `/freeze` 的限制。 |
| `/gstack-upgrade` | **自动更新** ——升级 gstack 到最新版本。自动检测全局安装还是项目内安装，同步两者，显示更新内容。 |

**[每个技能的深入解析与实例 →](docs/skills.md)**

## 新功能及其重要性

**`/office-hours` 在你写代码之前重新定义你的产品。** 你说"每日简报应用"。它倾听你的真实痛点，挑战你的表述，告诉你其实你要做的是一个个人首席幕僚 AI，质疑你的前提假设，并生成三种实现方案及工作量估算。它撰写的设计文档会直接传递给 `/plan-ceo-review` 和 `/plan-eng-review`——这样每个下游技能都从清晰的定义开始，而不是一个模糊的功能需求。

**设计是核心。** `/design-consultation` 不只是挑选字体。它会研究你所在领域的现有产品，提出安全的选择和创意冒险，生成你实际产品的真实样式，并撰写 `DESIGN.md`——然后 `/design-review` 和 `/plan-eng-review` 会读取你的设计决策。设计决策贯穿整个系统。

**`/qa` 是一个巨大的突破。** 它让我从 6 个并行工作者扩展到 12 个。Claude Code 说出*"我看到问题了"*，然后真的修复了它，生成了回归测试，并验证了修复——这改变了我的工作方式。智能体现在有"眼睛"了。

**智能审查路由。** 就像在一家运转良好的初创公司一样：CEO 不需要审查基础设施的 bug 修复，设计审查不需要看后端变更。gstack 追踪已执行的审查，判断什么是合适的，然后做出聪明的选择。审查就绪仪表盘会在你发布之前告诉你当前状态。

**测试一切。** `/ship` 会在项目没有测试框架的情况下从零搭建。每次 `/ship` 运行都会产出覆盖率审计。每个 `/qa` 的 bug 修复都会生成回归测试。100% 测试覆盖率是目标——测试让 vibe coding（氛围编程）变得安全，而不是 yolo coding（盲目编程）。

**`/document-release` 是你从未有过的工程师。** 它读取项目中的每个文档文件，与代码差异交叉对照，更新所有偏移的内容。README、ARCHITECTURE、CONTRIBUTING、CLAUDE.md、TODOS——全部自动保持最新。而且现在 `/ship` 会自动调用它——无需额外命令，文档就能保持同步。

**AI 卡住时的浏览器交接。** 遇到验证码、认证墙或多因素认证提示？`$B handoff` 会在完全相同的页面打开一个可见的 Chrome 窗口，保留所有 cookies 和标签页。解决问题后告诉 Claude 你完成了，`$B resume` 会从中断的地方继续。连续 3 次失败后，智能体甚至会自动建议这样做。

**多 AI 交叉验证。** `/codex` 从 OpenAI 的 Codex CLI 获取独立审查——一个完全不同的 AI 审查同一份代码差异。三种模式：带通过/失败门禁的代码审查、主动尝试破坏你代码的对抗性挑战、以及具有会话连续性的开放咨询。当 `/review`（Claude）和 `/codex`（OpenAI）都审查了同一分支时，你会得到跨模型分析，显示哪些发现是重叠的，哪些是各自独有的。

**按需启用安全护栏。** 说"小心点"，`/careful` 就会在任何破坏性命令前发出警告——rm -rf、DROP TABLE、force-push、git reset --hard。`/freeze` 在调试时将编辑锁定在一个目录内，防止 Claude 意外"修复"无关的代码。`/guard` 同时激活两者。`/investigate` 会自动冻结到正在调查的模块。

**主动技能建议。** gstack 会感知你当前所处的阶段——头脑风暴、审查、调试、测试——并建议合适的技能。不喜欢？说"别再建议了"，它会跨会话记住。

## 10-15 个并行冲刺

gstack 在单个冲刺中已经很强大。10 个同时运行时则是变革性的。

[Conductor](https://conductor.build) 可以并行运行多个 Claude Code 会话——每个都在独立的隔离工作区中。一个会话对新想法运行 `/office-hours`，另一个对 PR 做 `/review`，第三个在实现功能，第四个在测试环境运行 `/qa`，还有六个在其他分支上工作。全部同时进行。我经常运行 10-15 个并行冲刺——这是目前的实际上限。

冲刺结构正是让并行成为可能的关键。没有流程的话，十个智能体就是十个混乱源。有了流程——思考、规划、构建、审查、测试、发布——每个智能体都清楚地知道该做什么以及何时停止。你管理它们的方式就像 CEO 管理团队一样：把关重要决策，其余的让它们自行运转。

---

## 一起乘风破浪

这是**免费、MIT 许可证、开源、现在就可用的**。没有付费版。没有候补名单。没有附加条件。

我开源了我的开发方式，并且正在持续升级我自己的软件工厂。你可以 fork 它，让它成为你自己的。这就是全部意义。我希望每个人都加入这段旅程。

相同的工具，不同的结果——因为 gstack 给你的是结构化的角色和审查门禁，而不是通用的智能体混乱。这种治理就是快速发布和鲁莽发布之间的区别。

模型进步得很快。那些现在就搞清楚如何与它们合作的人——真正合作，而不是浅尝辄止——将拥有巨大的优势。现在就是那个窗口期。让我们出发吧。

15 个专家角色和 6 个强力工具。全部斜杠命令。全部 Markdown。全部免费。**[github.com/garrytan/gstack](https://github.com/garrytan/gstack)** —— MIT 许可证

> **我们在招聘。** 想要每天产出 10,000+ 行代码并帮助完善 gstack？
> 来 YC 工作吧 —— [ycombinator.com/software](https://ycombinator.com/software)
> 极具竞争力的薪资和股权。旧金山，Dogpatch 区。

## 文档

| 文档 | 内容 |
|------|------|
| [技能深入解析](docs/skills.md) | 每个技能的理念、示例和工作流（包括 Greptile 集成） |
| [架构](ARCHITECTURE.md) | 设计决策和系统内部机制 |
| [浏览器参考](BROWSER.md) | `/browse` 的完整命令参考 |
| [贡献指南](CONTRIBUTING.md) | 开发环境设置、测试、贡献者模式和开发模式 |
| [更新日志](CHANGELOG.md) | 每个版本的新功能 |

## 隐私与遥测

gstack 包含**可选加入**的使用遥测功能，用于帮助改进项目。具体如下：

- **默认关闭。** 除非你明确同意，否则不会向任何地方发送数据。
- **首次运行时，** gstack 会询问你是否愿意分享匿名使用数据。你可以拒绝。
- **发送的内容（如果你选择加入）：** 技能名称、持续时间、成功/失败、gstack 版本、操作系统。仅此而已。
- **永远不会发送的内容：** 代码、文件路径、仓库名称、分支名称、提示词或任何用户生成的内容。
- **随时更改：** `gstack-config set telemetry off` 立即禁用所有遥测。

数据存储在 [Supabase](https://supabase.com)（开源的 Firebase 替代品）中。数据表结构在 [`supabase/migrations/001_telemetry.sql`](supabase/migrations/001_telemetry.sql) 中——你可以验证具体收集了什么。仓库中的 Supabase 公开密钥是一个公开密钥（类似 Firebase API 密钥）——行级安全策略将其限制为仅插入访问。

**本地分析始终可用。** 运行 `gstack-analytics` 查看你从本地 JSONL 文件获取的个人使用仪表盘——无需远程数据。

## 故障排除

**技能没有出现？** `cd ~/.claude/skills/gstack && ./setup`

**`/browse` 失败？** `cd ~/.claude/skills/gstack && bun install && bun run build`

**安装过时？** 运行 `/gstack-upgrade` ——或在 `~/.gstack/config.yaml` 中设置 `auto_upgrade: true`

**Windows 用户：** gstack 可在 Windows 11 上通过 Git Bash 或 WSL 使用。除 Bun 外还需要 Node.js——Bun 在 Windows 上的 Playwright 管道传输有一个已知 bug（[bun#4253](https://github.com/oven-sh/bun/issues/4253)）。browse 服务器会自动回退到 Node.js。请确保 `bun` 和 `node` 都在你的 PATH 中。

**Claude 说看不到技能？** 确保你项目的 `CLAUDE.md` 有 gstack 章节。添加以下内容：

```
## gstack
Use /browse from gstack for all web browsing. Never use mcp__claude-in-chrome__* tools.
Available skills: /office-hours, /plan-ceo-review, /plan-eng-review, /plan-design-review,
/design-consultation, /review, /ship, /browse, /qa, /qa-only, /design-review,
/setup-browser-cookies, /retro, /investigate, /document-release, /codex, /careful,
/freeze, /guard, /unfreeze, /gstack-upgrade.
```

## 许可证

MIT。永久免费。去创造点什么吧。
