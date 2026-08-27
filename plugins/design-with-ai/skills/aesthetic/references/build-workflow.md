# Website implementation workflow

Use this workflow for both redesigns and greenfield websites. Scale the depth to the requested scope, but do not skip discovery or rendered verification.

## 1. Establish a baseline

Read the repository instructions and inspect the actual project before choosing a design or dependency.

- Check the working tree and preserve unrelated changes.
- Identify the framework, package manager, route structure, rendering mode, styling system, tokens, component primitives, icon set, fonts, tests, linting, and build commands.
- Trace the important user journeys and the business logic behind them.
- Run the existing fast checks. If the site runs, inspect representative routes before editing and retain screenshots when they will make comparison useful.
- List the pages and states in scope. Include loading, empty, error, permission, success, long-content, and narrow-screen states when they exist.

For greenfield work, choose the least complex stack that meets the brief. A current Next.js, TypeScript, and Tailwind setup is a sensible default for an interactive product site that needs routing, server rendering, or technical SEO. Do not use it when a static page or the client's required stack is simpler.

Before starting a greenfield build, confirm that the available brief establishes the site's purpose, audience, client identity, required routes or sections, primary actions, and factual content. Ask for the missing decisions when guessing would change the product or invent client claims. Placeholder content is acceptable only when the user requested a prototype and it is clearly labeled.

## 2. Set the direction

Extract useful signals from the product and client: audience, job, content, logo and assets, existing colors, market position, desired emotional tone, information density, and accessibility needs.

Write a short direction before coding. Define:

- type roles and scale;
- color roles and contrast behavior;
- spacing and layout rhythm;
- radii, borders, and elevation;
- icon treatment and imagery;
- density and responsive behavior;
- motion rules.

Use the strongest direction and proceed after satisfying the greenfield requirements gate above. Pause when essential product or brand input is absent and the plausible choices would create materially different products, factual claims, or client identities.

Avoid a generic "premium" skin. Gradients, glass panels, huge headlines, animated blobs, dense card grids, and excessive rounding are not quality by themselves. Use them only when the product direction supports them.

## 3. Decide whether outside components help

Inventory the project's existing primitives first. Prefer composition and improvement over replacement.

When a real gap remains:

1. Read [component-sources.md](component-sources.md).
2. Search the preferred sources that match the project stack and the interaction needed.
3. Choose one component foundation and no more than two accent sources.
4. Verify the official page, current license or terms, framework and version requirements, dependencies, accessibility behavior, and exact install or copy method.
5. Review the downloaded source and dependency diff before integrating it.

Do not copy screenshots, branded assets, or distinctive screens from inspiration catalogs. Translate the underlying hierarchy or interaction principle.

## 4. Implement from foundations outward

Work in this order unless the repository gives a better dependency order:

1. tokens, fonts, page background, focus style, and layout primitives;
2. shared shell, navigation, footer, and global feedback;
3. reusable controls and content components;
4. page sections and complete routes;
5. responsive and non-ideal states;
6. purposeful motion and final subtraction.

Use real client content when available. Preserve factual claims and working behavior. Remove placeholder names, demo data, library branding, unused variants, and copied code that the finished site does not need.

Keep presentation separate from domain logic. Do not replace a working data flow to make a component easier to install.

## 5. Record provenance

Create or update `UI-SOURCES.md` when external component code or design assets enter the project. This includes copied components, fonts, icon packs, stock images, templates, and hosted font or asset services. Verify reuse rights before integrating anything sourced by the agent. If the rights remain unclear, choose another source. User-supplied assets may be used within the requested project and should be recorded without inventing a license. A compact entry is enough:

```markdown
## Component name

- Source: https://official.example/component
- Retrieved: YYYY-MM-DD
- License: MIT
- Added with: `exact command` or `manual copy`
- Local files or runtime use: `path/to/component.tsx`
- Changes: adapted tokens, removed demo data, added reduced-motion behavior
```

For a hosted font or asset, record the provider URL, the exact family or asset, its verified terms, and where the project loads it. For an asset supplied directly by the user, write `Provided by client` instead of guessing its origin or license. Preserve copyright or license notices when the source requires them. Do not place tokens, license keys, or account credentials in this file or anywhere else in the repository.

## 6. Verify and hand off

Follow [visual-qa.md](visual-qa.md). Fix observed problems and repeat the relevant checks.

The handoff should state:

- the visual direction implemented;
- key files and routes changed;
- outside sources and dependencies used;
- build, test, lint, and accessibility checks run;
- exact desktop and mobile views inspected;
- remaining risks or unverified states.

Do not deploy or publish unless the user explicitly requested that action and the normal approval boundary has been satisfied.
