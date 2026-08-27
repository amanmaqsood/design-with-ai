# Design with AI

![Design with AI: a systems-oriented agent skill](assets/design-with-ai-cover.png)

Design with AI is a plugin for two related jobs. It can help decide what an interface should be, then turn that direction into working website code.

[Aman Maqsood](https://github.com/amanmaqsood) built it for Codex and Claude Code.

## Install

### Codex

```bash
codex plugin marketplace add amanmaqsood/design-with-ai && codex plugin add design-with-ai@amanmaqsood-design
```

### Claude Code

```bash
claude plugin marketplace add amanmaqsood/design-with-ai && claude plugin install design-with-ai@amanmaqsood-design
```

Run `/reload-plugins` if you install it during an active Claude Code session.

## Choose a skill

### Design with AI

Use this when you need direction, critique, or refinement before implementation.

Codex:

```text
$design-with-ai critique this checkout flow and recommend a coherent redesign
```

Claude Code:

```text
/design-with-ai:design-with-ai refine this dashboard without adding more UI
```

### Aesthetic

Use this when you want the agent to inspect a codebase, find suitable components, implement the website, run it, and check the rendered result.

Codex:

```text
$aesthetic make this entire website feel considered, premium, and specific to the client
```

Claude Code:

```text
/design-with-ai:aesthetic design better and implement the full site
```

Natural implementation requests such as "make this site aesthetic," "design this better," "give this website a premium UI," and "polish and build this website" can also trigger the skill. Advice-only questions continue to use the design skill.

## How Aesthetic works

For an existing project, the skill reads the framework, routes, components, styles, business logic, and current UI before choosing a direction. It preserves the stack and working behavior unless the user asks for a deeper change. It can also build a new website from scratch when the brief contains the essential product and client facts.

When the project needs outside components, the agent checks official sources, compatibility, and licensing before adding them. It uses one component foundation and no more than two justified accent sources, so the final site does not look assembled from unrelated demos.

The implementation covers shared foundations, responsive pages, loading and error states, accessibility basics, purposeful motion, performance risks, and technical SEO hygiene. The agent records outside component code, fonts, icons, images, and hosted design assets in `UI-SOURCES.md`.

Rendered verification is part of the job. The agent runs the site, checks representative desktop and mobile views, exercises important interactions, and runs the project's existing tests and production build. If it cannot inspect the rendered site, it must say that visual QA is incomplete.

## Component research

The preferred source catalog includes Beautiful UI, beUI, Rare UI, Transitions.dev, shadcn/ui, UI Skills, coss ui, ReUI, Canvas UI, Collect UI, Recent, Mobbin, and 60fps Design.

Some provide reusable code. Others are reference libraries, paid services, or authenticated MCPs. The skill verifies the current terms instead of assuming that everything visible online is free to copy. Paid tools remain optional, and the plugin does not bundle credentials or MCP dependencies.

The complete routing and licensing policy lives in [component-sources.md](plugins/design-with-ai/skills/aesthetic/references/component-sources.md).

## Repository structure

```text
.agents/plugins/marketplace.json                  Codex marketplace
.claude-plugin/marketplace.json                   Claude Code marketplace
plugins/design-with-ai/.codex-plugin/             Codex manifest
plugins/design-with-ai/.claude-plugin/            Claude Code manifest
plugins/design-with-ai/skills/design-with-ai/     Design and critique skill
plugins/design-with-ai/skills/aesthetic/          Website implementation skill
```

## Acknowledgments

![How I Design with AI title card](assets/how-i-design-with-ai-source.png)

Matt Dailey's *How I Design with AI* informed the first version of this project. The post covers whole-system constraints, subtraction, low-cost iteration, components, previews, precedents, and learned taste. Its constraint-first approach also draws on Christopher Alexander's *Notes on the Synthesis of Form*.

Aman Maqsood wrote and maintains this repository. Matt Dailey, Christopher Alexander's estate, Anthropic, and OpenAI are not affiliated with it and do not endorse it.

## License

[MIT](LICENSE)
