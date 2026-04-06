# Contributing to Awesome Design MD

Thanks for contributing.

This repository is a curated collection of DESIGN.md files extracted from popular websites. Each file captures a site's complete visual language — including accessibility, interaction patterns, and responsive behavior — in a format any AI agent can read.

## DESIGN.md Format (11 Sections)

Every DESIGN.md file must follow this structure. Sections 1-11 are mandatory.

| # | Section | Required content |
|---|---------|-----------------|
| 1 | Visual Theme & Atmosphere | Mood, density, design philosophy, key characteristics |
| 2 | Color Palette & Roles | Semantic name + hex + functional role for every color |
| 3 | Typography Rules | Font families, full hierarchy table (size, weight, line-height, letter-spacing), OpenType features, fluid type scale |
| 4 | Component Stylings | Buttons, cards, inputs, navigation — with all visual properties and states |
| 5 | Layout Principles | Spacing scale (with base unit), grid system, container widths, whitespace philosophy |
| 6 | Depth & Elevation | Shadow system with exact values, surface hierarchy table |
| 7 | Accessibility | WCAG target level, contrast ratios for all key pairings (with pass/fail), focus system, ARIA patterns, motion policy, minimum touch targets, screen reader guidance |
| 8 | Interaction Patterns | State machine table (default/hover/active/focus/disabled/loading), transition timing, modals, error states, loading states, empty states |
| 9 | Responsive Behavior | Breakpoints table, fluid typography (clamp values), dark mode tokens, container queries, touch target sizes (specific px), collapsing strategy |
| 10 | Do's and Don'ts | Design guardrails and anti-patterns specific to this design system |
| 11 | Agent Prompt Guide | Quick color reference, ready-to-use component prompts, accessibility prompt, iteration guide |

### Section 7 (Accessibility) Requirements

This section is not optional. Every DESIGN.md must include:

- **WCAG target**: State the target level (minimum AA)
- **Contrast ratios**: Calculate the ratio for every text-on-background pairing in the color palette. Mark each as Pass/Fail against WCAG AA (4.5:1 normal text, 3:1 large text). Flag any failing pairs with guidance on where they can safely be used.
- **Focus indicators**: Exact CSS for focus rings. Must be visible on all surface colors used in the system.
- **ARIA patterns**: Document expected roles, labels, and states for all components in section 4.
- **Motion policy**: Describe what changes under `prefers-reduced-motion: reduce`.
- **Touch targets**: Minimum dimensions in pixels (44x44px mobile per WCAG 2.5.8).
- **Screen reader guidance**: Heading hierarchy, alt text policy, aria-label requirements.

### Section 9 (Responsive) Requirements

- **Fluid typography**: At least display and heading sizes must use `clamp()` values.
- **Dark mode tokens**: Full color mapping for dark mode (background, text, borders, shadows, surfaces). Every DESIGN.md already has a `preview-dark.html` — the tokens must match.
- **Touch target sizes**: Specific pixel dimensions, not "comfortable padding" or "adequate spacing".

## How to Contribute

### Request a New Site

To request a DESIGN.md for a website, [open an issue](https://github.com/VoltAgent/awesome-design-md/issues/new?template=design-md-request.yml) with the website URL.

We receive many requests, and maintainer bandwidth is limited. Sponsor-backed requests are prioritized, consider supporting the project via [GitHub Sponsors](https://github.com/sponsors/VoltAgent) if you'd like faster turnaround.

### Improve an Existing DESIGN.md

If you notice issues with an existing file:

1. **Open an issue first** to describe what you'd like to change and get feedback from maintainers
2. Open the site's `DESIGN.md`
3. Compare against the live site
4. Fix incorrect hex values, missing tokens, or weak descriptions
5. Verify accessibility claims — check contrast ratios with a tool like [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)
6. Ensure all 11 sections are present and populated
7. Update the `preview.html` and `preview-dark.html` if your changes affect displayed tokens
8. Open a PR with before/after rationale

## Quality Checklist

Before submitting a PR, verify:

- [ ] All 11 sections present and numbered correctly
- [ ] Color contrast ratios calculated and marked Pass/Fail
- [ ] Focus system documented with exact CSS
- [ ] ARIA patterns specified for all components
- [ ] `prefers-reduced-motion` policy documented
- [ ] Touch targets specified in pixels (not "comfortable" or "adequate")
- [ ] Fluid typography uses `clamp()` for display/heading sizes
- [ ] Dark mode tokens documented
- [ ] Agent Prompt Guide includes accessibility prompt

## License

By contributing, you agree your contributions are provided under the repository license terms.
