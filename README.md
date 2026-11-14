# bbkan-design-skills

**A small visual design system for websites and posters, inspired by 不白看 (BBKan).**

It brings the site's warm paper surfaces, ink-like typography, deep blue window chrome, orange accents, square corners, and tactile inset borders into two practical formats: responsive web interfaces and print-ready posters. The goal is to preserve the visual character while adapting the layout to the job and the medium.

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
- `skills/bbkan-visual-design/references/poster.md` — hierarchy, composition, print sizes, and export checks.
- `skills/bbkan-visual-design/assets/bbkan-theme.css` — optional CSS variables and tactile border utilities for web work.
- `examples/` — short example briefs for trying both formats.

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

## License

Released under the [MIT License](LICENSE).

