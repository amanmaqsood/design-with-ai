# Rendered website QA

Use the strongest browser or visual inspection tool available. A source diff, green build, or preview URL cannot substitute for seeing the rendered interface.

## Start with the real project

- Run the repository's documented development command.
- Confirm the server is reachable and note the actual URL.
- Use representative data and the real routes in scope.
- Watch the terminal and browser console for runtime errors, failed requests, hydration problems, and warnings caused by the change.

## Inspect representative views

At minimum, inspect one narrow mobile viewport and one common desktop viewport. Add tablet, wide desktop, or embedded contexts when the product needs them.

For every important route or journey, check:

- visual hierarchy and primary action;
- typography, wrapping, truncation, and long content;
- spacing, alignment, density, and responsive reflow;
- navigation, focus order, keyboard operation, and visible focus;
- contrast, labels, landmarks, headings, and image alternatives;
- loading, empty, error, permission, success, and disabled states;
- overflow, sticky elements, dialogs, menus, forms, and destructive actions;
- motion purpose, interruption, reduced motion, and perceived speed;
- touch targets, hover-only behavior, and mobile input.

Exercise interactions instead of judging a static screenshot. Capture before and after images when they make a material change easier to verify.

Inspect the live rendered viewport at readable zoom or open its capture at a readable size. Check text and controls near every viewport edge. A matching `scrollWidth` and `clientWidth` does not prove that painted text, focus rings, transforms, or overlays are visible rather than clipped.

## Check technical quality

Run the project's existing formatter, type checker, linter, tests, and production build in proportion to the change. Do not introduce a new tool merely to produce a reassuring score.

Check technical SEO basics when the site is public-facing: meaningful page titles and descriptions, one clear page heading, semantic landmarks, indexability controls, canonical behavior where configured, and stable metadata after route changes.

Check performance risks introduced by the design: oversized images, layout shift, unnecessary client JavaScript, heavy animation, WebGL fallbacks, font loading, and unused component dependencies. Use existing performance tooling when available.

## Fix and repeat

Fix visible defects and rerun the affected viewport, interaction, and build checks. Avoid polishing one hero view while leaving the rest of the journey inconsistent.

## Evidence standard

Report facts, not confidence language. A useful final note names:

- the routes and viewport sizes actually inspected;
- interactions and states exercised;
- commands that passed or failed;
- console or runtime issues observed;
- visual checks that could not be performed.

If no visual tool is available, state that rendered QA is incomplete. Do not describe the site as polished, premium, production-ready, or fully verified.
