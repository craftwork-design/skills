<p align="center">
  <a href="https://craftwork.design/skill"><img src="logo.png" width="72" height="72" alt="Craftwork"></a>
</p>

<h1 align="center">Craftwork Design skill</h1>

<p align="center">
  An agent skill that makes interfaces built by Claude Code, Codex, Cursor and other agents look designed rather than generated.
</p>

```bash
npx skills add craftwork-design/skills
```

`craftwork-design` is an [agent skill](https://agentskills.io) for any agent that reads `SKILL.md`. Before writing code, the agent reads the brief and picks a design direction. It then studies real websites and templates, measures the one it follows, and builds with human-made resources from [Craftwork](https://craftwork.design): React components, templates, fonts, shader backgrounds, 3D, icons and mockups, instead of placeholders and hand-drawn effects.

## Before and after

Ask an agent for a landing page for Fieldnote, an AI note-taker for customer interviews. On its own, it falls back to the usual defaults: an "Advanced AI" badge, emoji icons, "Trusted by 10,000+ teams", made-up stats and a dashboard drawn from divs.

With the skill and the Craftwork MCP server, the same agent first states a design read you can correct, for example:

> Reading this as: B2B product landing for research teams, in a minimal language, with an outline icon pack, a geometric sans and the product screenshot in a device mockup as the hero.

Then it builds from a Framer template in the right style, adds a 3D studio microphone that follows the cursor because the copy is about recording calls, and takes every icon from one set. Both versions of the Fieldnote page are on [craftwork.design/mcp](https://craftwork.design/mcp).

## What the skill does

- **Reads the brief first.** Page kind, audience, style family and the page's one idea, from the product itself.
- **Starts from references.** Inspiration from real websites and sections, then Craftwork templates by genre and style. The lead reference is opened and measured: type, spacing, grid, buttons, hover timings.
- **Sources resources in order.** References, templates and layouts, animated React components, fonts, icons, shader backgrounds, mockups. 3D models and illustrations come last and only when a section's copy names their idea.
- **Keeps one visual system.** One locked style and theme, one icon pack, at most two font families, harmony checks so every image fits the subject, mood, scale and palette.
- **Leaves out the usual AI tells.** Default fonts, purple glows, gradient headlines, em dashes, middle-dot separators, three equal cards, fake screenshots, placeholder names and filler verbs.
- **Checks before it is done.** A pre-flight pass on screenshots: hovers, buttons, contrast, states, overflow, focus rings.
- **Respects your project.** If you already have tokens, fonts, an icon library or a component kit, the agent follows them and uses Craftwork only to fill gaps.

## Install

**skills CLI** (Claude Code, Codex, Cursor, OpenCode and other agents):

```bash
npx skills add craftwork-design/skills
```

**Claude Code plugin** (the skill and the Craftwork MCP server together):

```
/plugin marketplace add craftwork-design/skills
/plugin install craftwork@craftwork
```

**Craftwork wizard** (the skill and the MCP server for every agent it finds):

```bash
npx -y @craftwork-design/wizard@latest
```

**By hand:**

```bash
mkdir -p .claude/skills/craftwork-design && curl -L https://craftwork.design/SKILL.md -o .claude/skills/craftwork-design/SKILL.md
```

Then brief the agent the way you would brief a designer:

```
Build a pricing page for a budgeting app. Keep it calm and friendly.
```

## Craftwork MCP

The taste rules work on their own. To pull real files and code, connect the [Craftwork MCP server](https://github.com/craftwork-design/mcp) at `https://craftwork.design/api/mcp`. Searching is free with a Craftwork account, a free account also gets 5 premium assets a month, and [Pro](https://craftwork.design/pricing) opens every pack.

## Links

- Overview: https://craftwork.design/skill
- Docs: https://craftwork.design/skill/docs
- Changelog: https://craftwork.design/skill/changelog
- The live file: https://craftwork.design/SKILL.md

This repository mirrors the live file. Issues and suggestions are welcome here.

## License

MIT. Some taste rules are adapted from [taste-skill](https://github.com/Leonxlnx/taste-skill) (MIT).
