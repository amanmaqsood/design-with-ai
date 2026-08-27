# Design with AI

An agent skill for designing, critiquing, and refining product interfaces as coherent systems—not collections of familiar AI-generated components.

Built by [Aman Maqsood](https://github.com/amanmaqsood) for both Codex and Claude Code.

## Install

### Codex

```bash
codex plugin marketplace add amanmaqsood/design-with-ai && codex plugin add design-with-ai@amanmaqsood-design
```

Invoke it with `$design-with-ai`:

```text
$design-with-ai critique this checkout flow and recommend a coherent redesign
```

### Claude Code

```bash
claude plugin marketplace add amanmaqsood/design-with-ai && claude plugin install design-with-ai@amanmaqsood-design
```

Invoke the installed plugin skill with:

```text
/design-with-ai:design-with-ai refine this dashboard without adding more UI
```

Run `/reload-plugins` if installing inside an active Claude Code session.

## What it does

The skill supports three modes:

- **Design** a new interface from product constraints.
- **Critique** an existing screen, flow, prototype, or implementation.
- **Refine** a direction without accumulating local patches and unnecessary UI.

It helps the agent map the whole product system, explore materially different directions, subtract weak elements, establish reusable components, study relevant precedents, and validate realistic states in a working preview.

The skill has no runtime dependencies, MCP servers, telemetry, or network calls of its own. Its behavior remains subject to the permissions and tools available in the host.

## Repository structure

```text
.agents/plugins/marketplace.json             Codex marketplace
.claude-plugin/marketplace.json              Claude Code marketplace
plugins/design-with-ai/.codex-plugin/        Codex manifest
plugins/design-with-ai/.claude-plugin/       Claude Code manifest
plugins/design-with-ai/skills/design-with-ai Shared Agent Skill
```

## Acknowledgments

The initial spark came from Matt Dailey's *How I Design with AI* post and its discussion of whole-system constraints, subtraction, low-cost iteration, components, previews, precedents, and learned taste. The constraint-first perspective also points back to Christopher Alexander's *Notes on the Synthesis of Form*.

This repository is independently written and maintained by Aman Maqsood. It is not affiliated with or endorsed by Matt Dailey, Christopher Alexander's estate, Anthropic, or OpenAI.

## License

[MIT](LICENSE)
