---
name: aesthetic
description: Redesign and implement complete, polished websites in an existing or greenfield codebase. Use for an explicit website or codebase implementation request such as "make this site aesthetic," "design this better," "give this website a premium UI," or "polish and build this website"; use design-with-ai for advice, examples, critique, or direction without implementation.
---

# Aesthetic

Leave the user with working website code, not a moodboard or a list of suggestions. Build a coherent client-specific interface, use outside components only when they fit, and verify the rendered result.

## Protect the product

- Preserve working business logic, factual copy, supplied assets, analytics, and framework choices unless the user explicitly puts them in scope.
- In an existing project, adapt to its framework, styling system, component conventions, and package manager. Do not add React, Tailwind, or shadcn solely to reach a component catalog.
- For greenfield interactive product sites, prefer current Next.js, TypeScript, and Tailwind when no simpler stack fits better. Choose the least complex stack that satisfies the brief.
- Treat deployment, paid services, authenticated MCP setup, and framework replacement as separate approval points. If code or a design asset sourced by the agent has unclear license or reuse rights, do not use it; choose a clearly permitted source instead. A user-supplied asset may be used within the requested project, but record it as `Provided by client` and make no broader rights claim.

## Run the build

Read [references/build-workflow.md](references/build-workflow.md), then:

1. Inspect the repository, run its baseline checks, and identify the routes and states in scope.
2. Derive a visual direction from the client, content, product, and existing brand signals. State the direction briefly and proceed unless a missing brand decision would lead to materially different results.
3. Inventory existing primitives before adding anything. If a gap remains, read [references/component-sources.md](references/component-sources.md) and verify the current official source, compatibility, access, and license.
4. Implement foundations and shared components before page-level polish. Preserve behavior while improving hierarchy, typography, spacing, color roles, density, responsiveness, states, and purposeful motion.
5. Read [references/visual-qa.md](references/visual-qa.md), run the site, inspect it at representative desktop and mobile sizes, exercise important states, and run the project's build and tests.
6. Report the files changed, outside components used, checks run, rendered views inspected, and anything that remains unverified.

## Keep the system coherent

Use one component foundation and at most two accent sources. More sources require a concrete gap that the current system cannot solve. Adapt imported components to the same tokens and interaction rules; remove demo branding, dead variants, and unnecessary dependencies.

Create or update `UI-SOURCES.md` when external component code, fonts, icons, images, templates, or hosted design assets enter the client project. Record the official URL, retrieval date, verified license or terms, install or copy method, local destination or runtime use, and meaningful modifications. Mark user-supplied assets as `Provided by client` when no public source exists; do not invent a license. Preserve required notices.

Motion must explain change, maintain spatial context, or provide useful feedback. Keep frequent and keyboard-driven actions immediate, support reduced motion, and remove effects that hurt responsiveness or clarity.

## Use agents when useful

When the host supports parallel agents, divide bounded work into source research, non-overlapping implementation lanes, and an independent visual QA pass. Do not let agents edit the same files concurrently. Use the same workflow sequentially when subagents are unavailable; completion does not depend on a particular orchestration feature.

## Do not overclaim

A successful build proves that the project compiles. It does not prove that the website looks good or works through the whole journey. If rendered inspection is unavailable, finish safe code and build checks, then state that visual QA is incomplete.
