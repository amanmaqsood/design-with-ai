---
name: design-with-ai
description: Design, critique, or refine product interfaces as coherent systems. Use for UI/UX direction, product flows, interface reviews, design-to-code planning, or reducing generic and cluttered AI-generated UI; do not use for brand-only graphics.
---

# Design with AI

Create an interface whose hierarchy, behavior, and visual language follow from the product rather than from familiar templates.

## Choose the mode

- **Design**: turn a new product problem or feature into an interface direction and implementation-ready specification.
- **Critique**: diagnose an existing screen, flow, prototype, or implementation. Read [references/interface-review.md](references/interface-review.md) before reviewing.
- **Refine**: improve an existing direction while preserving its sound constraints and removing local fixes that weakened the whole.

If the request includes implementation, inspect the actual codebase and design system before proposing components. Do not assume a particular design tool or frontend stack.

## Establish the system

Before drawing or editing, write a compact constraint map:

- user and job to be done;
- primary action and information priority;
- required content, workflows, and business rules;
- important empty, loading, error, permission, success, and edge states;
- device, accessibility, platform, brand, and existing-component constraints;
- what must remain unchanged.

Separate facts from assumptions and decisions. Ask only for decisions that materially alter the result; discover repository and environment facts directly.

When feedback adds, removes, or changes a constraint, reconsider the composition that depends on it. Do not keep patching individual elements if the underlying hierarchy has changed.

## Explore before converging

For a substantial design decision, produce three meaningfully different directions. Vary the information model, interaction model, or hierarchy—not merely colors and spacing. For each direction, state:

- the organizing idea;
- which constraints it serves best;
- its cost or failure mode.

Recommend one direction plainly. Keep rejected directions only when their tradeoffs help the user decide.

Use the cheapest environment that gives adequate control: a design tool, a disposable HTML prototype, a component sandbox, or a temporary route. Avoid letting the first production implementation become the default simply because it already exists.

## Make every element earn its place

Perform a subtraction pass before adding polish. For every label, helper sentence, divider, icon, badge, card, control, and repeated action, ask what user decision or action it enables. Remove it when hierarchy, grouping, position, or a familiar control communicates the same thing.

Do not compensate for weak hierarchy with extra containers, gradients, oversized headings, decorative metrics, or explanatory copy. Prefer fewer, stronger signals.

## Build a visual language

Reuse existing primitives when they fit. If no coherent system exists, define the smallest useful set of tokens and components before composing many screens.

Keep product logic separate from presentation. Exercise new components in isolation with realistic variants and states, then connect them to product behavior. Record any deliberate exception to the shared system.

Study relevant precedents for interaction patterns and information density. Identify what principle transfers and what is product-specific. Adapt the principle; do not copy branded expression or proprietary assets.

## Validate the real experience

Review a working preview when one can be produced safely. Use representative data rather than ideal placeholder content. Check the complete journey, not only the hero state:

- narrow and wide layouts;
- long, short, missing, and malformed content;
- keyboard navigation, focus, contrast, labels, and motion preferences;
- latency, empty results, errors, permissions, and recovery;
- destructive actions, confirmations, and undo where relevant.

Treat a preview URL, successful build, or matching screenshot as evidence of availability—not proof of usability. Report what was actually exercised.

## Deliver the decision

Return only the sections the task needs, using this order when a full design handoff is useful:

1. **Design read** — user, job, constraints, and the central problem.
2. **Direction** — recommendation and why it wins over the alternatives.
3. **Interface specification** — hierarchy, layout, behavior, components, states, and essential copy.
4. **Subtraction log** — notable elements removed or consolidated and why.
5. **Validation** — evidence gathered, unresolved risks, and the next test.

Make the recommendation concrete enough to implement. Mark uncertain choices as hypotheses instead of disguising them as design principles.

## Grow judgment

After meaningful user feedback or validation, capture the reaction as a reusable principle: what felt wrong, what changed, and why the revision worked better. Prefer a small set of demonstrated principles over a large collection of fashionable rules.
