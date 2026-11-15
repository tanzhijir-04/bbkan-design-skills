# bbkan-design-skills

**纸窗蓝 · BBKan Paperframe** — 以「不白看」为灵感的网页与海报视觉设计 Skill。

[中文](#中文) · [English](#english) · [查看不白看示例网站](https://bbkan.2030036732.workers.dev/) · [支持作者](https://ifdian.net/a/tanz666)

![纸窗蓝视觉风格：窗口、配色与组件示例](https://raw.githubusercontent.com/tanzhijir-04/zhijir_imgur/main/img/20261115144558286.png)

## 中文

**纸窗蓝（BBKan Paperframe）** 是本项目为这套视觉语言取的名字：「纸」代表温暖的纸面底色与编辑式排版，「窗蓝」来自深蓝色的复古窗口。BBKan Design Skills 将这些特征与橙色点缀、硬边框整理成可复用的设计指导，适用于网页界面与海报。它帮助 AI 编程或设计助手理解这套视觉语言，并结合项目内容重新设计。

**在线参考：**[不白看 · 发现值得认真看的内容](https://bbkan.2030036732.workers.dev/)。

**网站白色模式截图**（保存于 2026 年 11 月 14 日）：

<img src="docs/images/bbkan-home-preview.png" alt="不白看网站首页白色模式截图" width="560">

### 安装

#### 方法一：通过 Skills CLI 安装（推荐）

需要 Node.js 22.20 或更新版本。在项目目录中打开终端，运行：

```bash
npx skills add tanzhijir-04/bbkan-design-skills --skill bbkan-visual-design
```

按照提示选择使用的 AI 助手和安装范围。要直接安装到 Codex 的用户级目录，供多个项目使用：

```bash
npx skills add tanzhijir-04/bbkan-design-skills --skill bbkan-visual-design --agent codex --global --yes
```

安装到 Claude Code 的用户级目录：

```bash
npx skills add tanzhijir-04/bbkan-design-skills --skill bbkan-visual-design --agent claude-code --global --yes
```

去掉 `--global` 可安装到当前项目。安装后建议开启新的助手会话；如需了解更多选项，可运行 `npx skills --help`。

#### 方法二：手动安装

下载或克隆本仓库，将 `skills/bbkan-visual-design` 整个文件夹复制到对应位置：

| 助手与范围 | 安装路径 |
| --- | --- |
| Codex：当前项目 | `<项目目录>/.agents/skills/bbkan-visual-design/` |
| Codex：所有项目 | `~/.agents/skills/bbkan-visual-design/` |
| Claude Code：当前项目 | `<项目目录>/.claude/skills/bbkan-visual-design/` |
| Claude Code：所有项目 | `~/.claude/skills/bbkan-visual-design/` |

请保留文件夹中的 `SKILL.md`、`references/` 和 `assets/`，然后启动新的助手会话。

### 使用

直接告诉助手使用「纸窗蓝」或「不白看视觉风格」，或在支持显式调用的助手中输入：

```text
$bbkan-visual-design 用不白看的视觉风格，为社区图书交换设计一个响应式首页。
```

```text
$bbkan-visual-design 用不白看的视觉风格，设计一张 A3 竖版独立电影放映海报。
```

Skill 会根据网页或海报读取相应的设计指南。它提供颜色、字体、排版、组件和输出建议，不要求使用「不白看」的标志或照搬网站内容。

### 包含什么

- [`SKILL.md`](skills/bbkan-visual-design/SKILL.md)：共享视觉原则及网页、海报的使用指引。
- [`references/web.md`](skills/bbkan-visual-design/references/web.md)：网页布局、组件状态与响应式设计。
- [`references/motion.md`](skills/bbkan-visual-design/references/motion.md)：非线性缓动、交互时长与减少动态效果的处理。
- [`references/poster.md`](skills/bbkan-visual-design/references/poster.md)：海报构图、信息层级与输出要点。
- [`assets/bbkan-theme.css`](skills/bbkan-visual-design/assets/bbkan-theme.css)：可选的网页颜色变量与立体边框样式。
- [`assets/bbkan-motion.css`](skills/bbkan-visual-design/assets/bbkan-motion.css)：可选的缓动变量和交互动效预设。
- [`examples/`](examples/)：网页和海报的示例提示词。

**动效覆盖范围：**提供基于原网站曲线的交互与数字滚动缓动，以及面板进入、退出和状态移动的建议预设；附 CSS 变量、可选类和减少动态效果的处理。更多用法见 [动效指南](skills/bbkan-visual-design/references/motion.md)。

### 作者与支持

作者：**Zhijie Tan**（[@tanzhijir-04](https://github.com/tanzhijir-04)）。如果这个项目对你有帮助，欢迎通过 [爱发电 · tanz666](https://ifdian.net/a/tanz666) 支持，也欢迎在 GitHub 给仓库点 Star。

### 赞助商招募

本项目正在寻找赞助商，欢迎希望支持开源设计工具的个人、团队或品牌通过 [作者 GitHub 主页](https://github.com/tanzhijir-04) 或 [爱发电](https://ifdian.net/a/tanz666) 联系作者，商讨赞助合作。

| 赞助商 | 展示位 |
| --- | --- |
| 待招募 | 在此展示赞助商名称、标志及链接 |

### 开源许可

本项目采用 [MIT License](LICENSE)。

---

## English

**BBKan Paperframe** is a visual design language for websites and posters, inspired by 不白看 (BBKan). Its Chinese name, **纸窗蓝**, brings together paper, windows, and blue.

It brings the site's warm paper surfaces, ink-like typography, deep blue window chrome, orange accents, square corners, and tactile inset borders into two practical formats: responsive web interfaces and print-ready posters. The goal is to preserve the visual character while adapting the layout to the job and the medium.

**Live reference:** [Visit 不白看 (BBKan)](https://bbkan.2030036732.workers.dev/).

## Install

### Recommended: install with the Skills CLI

You need Node.js 22.20 or newer. From your project directory, run:

```bash
npx skills add tanzhijir-04/bbkan-design-skills --skill bbkan-visual-design
```

The installer will ask which agent and whether to install for the current project or for your user account. To install globally for Codex without prompts:

```bash
npx skills add tanzhijir-04/bbkan-design-skills --skill bbkan-visual-design --agent codex --global --yes
```

For Claude Code, replace `codex` with `claude-code`:

```bash
npx skills add tanzhijir-04/bbkan-design-skills --skill bbkan-visual-design --agent claude-code --global --yes
```

Omit `--global` to install into the current project. Add more supported agent names after `--agent` if you use several agents. Run `npx skills --help` for the current CLI options.

### Manual installation

Download or clone this repository, then copy the `skills/bbkan-visual-design` directory into your agent's skills directory:

| Scope | Directory |
| --- | --- |
| Codex, current project | `<project>/.agents/skills/bbkan-visual-design/` |
| Codex, all projects | `~/.agents/skills/bbkan-visual-design/` |
| Claude Code, current project | `<project>/.claude/skills/bbkan-visual-design/` |
| Claude Code, all projects | `~/.claude/skills/bbkan-visual-design/` |

Keep the full folder, including `SKILL.md`, `references/`, and `assets/`. Start a new agent session after copying it so the skill can be discovered.

## Use it

Ask for the design style by name, or invoke the skill directly if your agent supports that syntax:

```text
$bbkan-visual-design Create a responsive homepage for a neighborhood book exchange.
```

```text
$bbkan-visual-design Design an A3 portrait poster for a weekend independent film screening.
```

The skill first identifies the medium and its constraints, then applies the shared design language with the relevant web or poster guidance. It can also use the system as a visual reference for new content; it does not require copying the 不白看 logo or page layout.

## What's included

- `skills/bbkan-visual-design/SKILL.md` — shared design principles and routing for websites and posters.
- `skills/bbkan-visual-design/references/web.md` — page structure, components, responsive behavior, and interaction states.
- `skills/bbkan-visual-design/references/motion.md` — nonlinear easing, interaction timing, and reduced-motion guidance.
- `skills/bbkan-visual-design/references/poster.md` — hierarchy, composition, print sizes, and export checks.
- `skills/bbkan-visual-design/assets/bbkan-theme.css` — optional CSS variables and tactile border utilities for web work.
- `skills/bbkan-visual-design/assets/bbkan-motion.css` — optional easing tokens and motion utilities.
- `examples/` — short example briefs for trying both formats.

**Motion coverage:** Includes interaction and number-reel easing based on the original site, suggested panel and state-change presets, CSS utilities, and reduced-motion behavior. See the [motion guide](skills/bbkan-visual-design/references/motion.md).

## Design tokens

| Role | Light | Dark |
| --- | --- | --- |
| Canvas | `#F1EEE5` | `#1D211F` |
| Surface | `#FFFCF5` | `#282F2B` |
| Paper | `#F8F5ED` | `#222824` |
| Ink | `#222923` | `#ECEAE3` |
| Muted text | `#77776D` | `#B5BCB2` |
| Blue | `#17439A` | `#244A82` |
| Deep blue | `#123779` | `#173865` |
| Orange | `#F26A32` | `#FF884F` |
| Rule | `#D2CFC3` | `#48514A` |

For posters, treat these as a palette rather than fixed screen colors: check contrast and adjust for the printer, paper, and viewing distance.

## Author

Created by **Zhijie Tan** ([@tanzhijir-04](https://github.com/tanzhijir-04)).

If this skill helps your work, you can support its creator at [爱发电 · tanz666](https://ifdian.net/a/tanz666).

## Sponsors wanted

We are looking for sponsors to support this open-source project. Individuals, teams, and brands can reach out via the [author's GitHub profile](https://github.com/tanzhijir-04) or [Afdian](https://ifdian.net/a/tanz666) to discuss sponsorship.

| Sponsor | Placement |
| --- | --- |
| Open for sponsorship | Your name, logo, and link can appear here. |

## License

Released under the [MIT License](LICENSE).

