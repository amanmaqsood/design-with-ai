# Component and reference sources

Use this as a routing catalog, not as proof that a component is still compatible or licensed the same way. Recheck the official source at implementation time. Prefer current official documentation, repositories, registries, and terms.

## Selection order

1. Reuse the project's existing component system.
2. Fill ordinary primitive gaps from the project's established registry or an accessible foundation such as shadcn/ui.
3. Add a specialized component only when it solves a specific interaction or composition gap.
4. Use inspiration and motion references to inform decisions, never as permission to copy.

Keep one foundation and at most two accent sources.

## Reusable code sources

| Source | Best use | Access and constraints |
| --- | --- | --- |
| [Beautiful UI](https://beautifului.dev) | AI chat, approval, reasoning, task, and agent-status primitives | MIT manual copy for React-style projects. Inspect imports and styling assumptions; no official installer or MCP is documented. |
| [beUI](https://beui.dev) | Animated React and Next.js accents | Free registry is MIT and targets React 19, Motion, and Tailwind 4. Pro is paid and credentialed. Use free entries unless the user authorizes existing Pro access. |
| [Rare UI](https://rareui.com) | Unusual animated React accents | Registry components are MIT with anti-resale terms. Review the component's provenance and dependencies. |
| [Transitions.dev](https://transitions.dev) | Purposeful CSS and React transition recipes | Product use is allowed for content the user can access; redistribution of the library is restricted. Free and Pro access differ. |
| [shadcn/ui](https://ui.shadcn.com) | Accessible React and Tailwind primitives and blocks | MIT open code with an official CLI, registry, skill, and MCP. Review community registry code before accepting it. |
| [coss ui](https://coss.com/ui) | Base UI and Tailwind product primitives | The `apps/ui` source is MIT; the wider monorepo uses other licensing, including AGPL. Install only documented UI registry entries. |
| [ReUI](https://reui.io/components) | Data-heavy product surfaces and application compositions | React 19 and Tailwind 4. Free and paid entries share a registry. MCP access requires an account; premium content requires entitlement. |
| [Canvas UI](https://canvasui.dev) | Focal Canvas or WebGL hero effects | Supports several web frameworks. License is MIT plus Commons Clause, so app use is allowed but component redistribution is restricted. Test fallbacks and GPU cost. |

Examples of official install paths may include `shadcn add` or a registry-specific command, but commands and package requirements can change. Copy the exact current command from the official component page instead of inventing one.

## Knowledge and audit sources

- [You Don't Need Animations](https://emilkowal.ski/ui/you-dont-need-animations): use its motion decision principles in original language. The article is not a component library.
- [UI Skills](https://ui-skills.com): fetch the smallest relevant design-engineering skill. Check the upstream skill's license before redistributing its text.
- [Design System Checklist](https://designsystemchecklist.com): use it to find gaps in foundations, components, documentation, accessibility, and governance. No explicit repository license was visible during the 2026-08-27 audit, so do not copy its full text.

## Inspiration-only sources

- [Collect UI](https://collectui.com)
- [Recent](https://recent.design)
- [Mobbin MCP](https://mobbin.com/mcp)
- [60fps Design MCP](https://60fps.design/mcp)

Use these to compare hierarchy, density, navigation, content structure, and interaction ideas. Do not copy screenshots, artwork, logos, text, or a distinctive screen wholesale. Mobbin and 60fps require paid access; 60fps motion code may target SwiftUI rather than the web.

## Authenticated and paid access

The public skill must work without paid services. Use a paid registry, private skill, MCP, OAuth flow, or token only when the user already has access and explicitly authorizes it.

- Mobbin MCP requires a paid plan and browser authorization.
- 60fps MCP requires a Pro subscription and authentication.
- ReUI MCP requires an account even when using its free request allowance; premium content needs a license.
- beUI Pro and Transitions Pro require their own entitlements.

Never scrape premium content, bypass access controls, ask the user to paste a secret into chat, or commit credentials. Fall back to public official sources.

## Install review

Before running a component installer or accepting copied source:

- confirm framework and version compatibility;
- read the actual license or terms for that component and subdirectory;
- inspect the command, generated files, scripts, dependency changes, and remote registry;
- check accessibility, reduced motion, mobile behavior, and browser support;
- remove demo branding, analytics, dead variants, and unrelated dependencies;
- add the item to `UI-SOURCES.md` and preserve required notices.

Treat service limits, prices, endpoints, plan names, and library requirements as changeable facts. Verify them live instead of relying on this catalog.
