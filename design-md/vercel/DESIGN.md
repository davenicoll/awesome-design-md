# Design System Inspiration of Vercel

## 1. Visual Theme & Atmosphere

Vercel's website is the visual thesis of developer infrastructure made invisible — a design system so restrained it borders on philosophical. The page is overwhelmingly white (`#ffffff`) with near-black (`#171717`) text, creating a gallery-like emptiness where every element earns its pixel. This isn't minimalism as decoration; it's minimalism as engineering principle. The Geist design system treats the interface like a compiler treats code — every unnecessary token is stripped away until only structure remains.

The custom Geist font family is the crown jewel. Geist Sans uses aggressive negative letter-spacing (-2.4px to -2.88px at display sizes), creating headlines that feel compressed, urgent, and engineered — like code that's been minified for production. At body sizes, the tracking relaxes but the geometric precision persists. Geist Mono completes the system as the monospace companion for code, terminal output, and technical labels. Both fonts enable OpenType `"liga"` (ligatures) globally, adding a layer of typographic sophistication that rewards close reading.

What distinguishes Vercel from other monochrome design systems is its shadow-as-border philosophy. Instead of traditional CSS borders, Vercel uses `box-shadow: 0px 0px 0px 1px rgba(0,0,0,0.08)` — a zero-offset, zero-blur, 1px-spread shadow that creates a border-like line without the box model implications. This technique allows borders to exist in the shadow layer, enabling smoother transitions, rounded corners without clipping, and a subtler visual weight than traditional borders. The entire depth system is built on layered, multi-value shadow stacks where each layer serves a specific purpose: one for the border, one for soft elevation, one for ambient depth.

**Key Characteristics:**
- Geist Sans with extreme negative letter-spacing (-2.4px to -2.88px at display) — text as compressed infrastructure
- Geist Mono for code and technical labels with OpenType `"liga"` globally
- Shadow-as-border technique: `box-shadow 0px 0px 0px 1px` replaces traditional borders throughout
- Multi-layer shadow stacks for nuanced depth (border + elevation + ambient in single declarations)
- Near-pure white canvas with `#171717` text — not quite black, creating micro-contrast softness
- Workflow-specific accent colors: Ship Red (`#ff5b4f`), Preview Pink (`#de1d8d`), Develop Blue (`#0a72ef`)
- Focus ring system using `hsla(212, 100%, 48%, 1)` — a saturated blue for accessibility
- Pill badges (9999px) with tinted backgrounds for status indicators

## 2. Color Palette & Roles

### Primary
- **Vercel Black** (`#171717`): Primary text, headings, dark surface backgrounds. Not pure black — the slight warmth prevents harshness.
- **Pure White** (`#ffffff`): Page background, card surfaces, button text on dark.
- **True Black** (`#000000`): Secondary use, `--geist-console-text-color-default`, used in specific console/code contexts.

### Workflow Accent Colors
- **Ship Red** (`#ff5b4f`): `--ship-text`, the "ship to production" workflow step — warm, urgent coral-red.
- **Preview Pink** (`#de1d8d`): `--preview-text`, the preview deployment workflow — vivid magenta-pink.
- **Develop Blue** (`#0a72ef`): `--develop-text`, the development workflow — bright, focused blue.

### Console / Code Colors
- **Console Blue** (`#0070f3`): `--geist-console-text-color-blue`, syntax highlighting blue.
- **Console Purple** (`#7928ca`): `--geist-console-text-color-purple`, syntax highlighting purple.
- **Console Pink** (`#eb367f`): `--geist-console-text-color-pink`, syntax highlighting pink.

### Interactive
- **Link Blue** (`#0072f5`): Primary link color with underline decoration.
- **Focus Blue** (`hsla(212, 100%, 48%, 1)`): `--ds-focus-color`, focus ring on interactive elements.
- **Ring Blue** (`rgba(147, 197, 253, 0.5)`): `--tw-ring-color`, Tailwind ring utility.

### Neutral Scale
- **Gray 900** (`#171717`): Primary text, headings, nav text.
- **Gray 600** (`#4d4d4d`): Secondary text, description copy.
- **Gray 500** (`#666666`): Tertiary text, muted links.
- **Gray 400** (`#808080`): Placeholder text, disabled states.
- **Gray 100** (`#ebebeb`): Borders, card outlines, dividers.
- **Gray 50** (`#fafafa`): Subtle surface tint, inner shadow highlight.

### Surface & Overlay
- **Overlay Backdrop** (`hsla(0, 0%, 98%, 1)`): `--ds-overlay-backdrop-color`, modal/dialog backdrop.
- **Selection Text** (`hsla(0, 0%, 95%, 1)`): `--geist-selection-text-color`, text selection highlight.
- **Badge Blue Bg** (`#ebf5ff`): Pill badge background, tinted blue surface.
- **Badge Blue Text** (`#0068d6`): Pill badge text, darker blue for readability.

### Shadows & Depth
- **Border Shadow** (`rgba(0, 0, 0, 0.08) 0px 0px 0px 1px`): The signature — replaces traditional borders.
- **Subtle Elevation** (`rgba(0, 0, 0, 0.04) 0px 2px 2px`): Minimal lift for cards.
- **Card Stack** (`rgba(0,0,0,0.08) 0px 0px 0px 1px, rgba(0,0,0,0.04) 0px 2px 2px, rgba(0,0,0,0.04) 0px 8px 8px -8px, #fafafa 0px 0px 0px 1px`): Full multi-layer card shadow.
- **Ring Border** (`rgb(235, 235, 235) 0px 0px 0px 1px`): Light gray ring-border for tabs and images.

## 3. Typography Rules

### Font Family
- **Primary**: `Geist`, with fallbacks: `Arial, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol`
- **Monospace**: `Geist Mono`, with fallbacks: `ui-monospace, SFMono-Regular, Roboto Mono, Menlo, Monaco, Liberation Mono, DejaVu Sans Mono, Courier New`
- **OpenType Features**: `"liga"` enabled globally on all Geist text; `"tnum"` for tabular numbers on specific captions.

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|------|--------|-------------|----------------|-------|
| Display Hero | Geist | 48px (3.00rem) | 600 | 1.00–1.17 (tight) | -2.4px to -2.88px | Maximum compression, billboard impact |
| Section Heading | Geist | 40px (2.50rem) | 600 | 1.20 (tight) | -2.4px | Feature section titles |
| Sub-heading Large | Geist | 32px (2.00rem) | 600 | 1.25 (tight) | -1.28px | Card headings, sub-sections |
| Sub-heading | Geist | 32px (2.00rem) | 400 | 1.50 | -1.28px | Lighter sub-headings |
| Card Title | Geist | 24px (1.50rem) | 600 | 1.33 | -0.96px | Feature cards |
| Card Title Light | Geist | 24px (1.50rem) | 500 | 1.33 | -0.96px | Secondary card headings |
| Body Large | Geist | 20px (1.25rem) | 400 | 1.80 (relaxed) | normal | Introductions, feature descriptions |
| Body | Geist | 18px (1.13rem) | 400 | 1.56 | normal | Standard reading text |
| Body Small | Geist | 16px (1.00rem) | 400 | 1.50 | normal | Standard UI text |
| Body Medium | Geist | 16px (1.00rem) | 500 | 1.50 | normal | Navigation, emphasized text |
| Body Semibold | Geist | 16px (1.00rem) | 600 | 1.50 | -0.32px | Strong labels, active states |
| Button / Link | Geist | 14px (0.88rem) | 500 | 1.43 | normal | Buttons, links, captions |
| Button Small | Geist | 14px (0.88rem) | 400 | 1.00 (tight) | normal | Compact buttons |
| Caption | Geist | 12px (0.75rem) | 400–500 | 1.33 | normal | Metadata, tags |
| Mono Body | Geist Mono | 16px (1.00rem) | 400 | 1.50 | normal | Code blocks |
| Mono Caption | Geist Mono | 13px (0.81rem) | 500 | 1.54 | normal | Code labels |
| Mono Small | Geist Mono | 12px (0.75rem) | 500 | 1.00 (tight) | normal | `text-transform: uppercase`, technical labels |
| Micro Badge | Geist | 7px (0.44rem) | 700 | 1.00 (tight) | normal | `text-transform: uppercase`, tiny badges |

### Principles
- **Compression as identity**: Geist Sans at display sizes uses -2.4px to -2.88px letter-spacing — the most aggressive negative tracking of any major design system. This creates text that feels _minified_, like code optimized for production. The tracking progressively relaxes as size decreases: -1.28px at 32px, -0.96px at 24px, -0.32px at 16px, and normal at 14px.
- **Ligatures everywhere**: Every Geist text element enables OpenType `"liga"`. Ligatures aren't decorative — they're structural, creating tighter, more efficient glyph combinations.
- **Three weights, strict roles**: 400 (body/reading), 500 (UI/interactive), 600 (headings/emphasis). No bold (700) except for tiny micro-badges. This narrow weight range creates hierarchy through size and tracking, not weight.
- **Mono for identity**: Geist Mono in uppercase with `"tnum"` or `"liga"` serves as the "developer console" voice — compact technical labels that connect the marketing site to the product.

### Font Loading Strategy
- **Display strategy**: `font-display: swap` for Geist Sans and Geist Mono — text renders immediately in the fallback (Arial) and swaps when the custom font loads
- **Preload**: `<link rel="preload" href="geist-sans.woff2" as="font" type="font/woff2" crossorigin>` for the primary weight (400) to minimize FOUT duration
- **Fallback alignment**: The fallback stack (`Arial, Apple Color Emoji, Segoe UI Emoji`) is chosen for metric compatibility with Geist — similar x-height and cap-height minimize layout shift on swap
- **Subset**: Serve Latin subset by default; load extended character sets on demand for internationalized content

## 4. Component Stylings

### Buttons

**Primary White (Shadow-bordered)**
- Background: `#ffffff`
- Text: `#171717`
- Padding: 0px 6px (minimal — content-driven width)
- Radius: 6px (subtly rounded)
- Shadow: `rgb(235, 235, 235) 0px 0px 0px 1px` (ring-border)
- Hover: background shifts to `var(--ds-gray-1000)` (dark)
- Focus: `2px solid var(--ds-focus-color)` outline + `var(--ds-focus-ring)` shadow
- Use: Standard secondary button

**Primary Dark (Inferred from Geist system)**
- Background: `#171717`
- Text: `#ffffff`
- Padding: 8px 16px
- Radius: 6px
- Use: Primary CTA ("Start Deploying", "Get Started")

**Pill Button / Badge**
- Background: `#ebf5ff` (tinted blue)
- Text: `#0068d6`
- Padding: 0px 10px
- Radius: 9999px (full pill)
- Font: 12px weight 500
- Use: Status badges, tags, feature labels

**Large Pill (Navigation)**
- Background: transparent or `#171717`
- Radius: 64px–100px
- Use: Tab navigation, section selectors

### Cards & Containers
- Background: `#ffffff`
- Border: via shadow — `rgba(0, 0, 0, 0.08) 0px 0px 0px 1px`
- Radius: 8px (standard), 12px (featured/image cards)
- Shadow stack: `rgba(0,0,0,0.08) 0px 0px 0px 1px, rgba(0,0,0,0.04) 0px 2px 2px, #fafafa 0px 0px 0px 1px`
- Image cards: `1px solid #ebebeb` with 12px top radius
- Hover: subtle shadow intensification

### Inputs & Forms
- Radio: standard styling with focus `var(--ds-gray-200)` background
- Focus shadow: `1px 0 0 0 var(--ds-gray-alpha-600)`
- Focus outline: `2px solid var(--ds-focus-color)` — consistent blue focus ring
- Border: via shadow technique, not traditional border

### Navigation
- Clean horizontal nav on white, sticky
- Vercel logotype left-aligned, 262x52px
- Links: Geist 14px weight 500, `#171717` text
- Active: weight 600 or underline
- CTA: dark pill buttons ("Start Deploying", "Contact Sales")
- Mobile: hamburger menu collapse
- Product dropdowns with multi-level menus

### Image Treatment
- Product screenshots with `1px solid #ebebeb` border
- Top-rounded images: `12px 12px 0px 0px` radius
- Dashboard/code preview screenshots dominate feature sections
- Soft gradient backgrounds behind hero images (pastel multi-color)

### Distinctive Components

**Workflow Pipeline**
- Three-step horizontal pipeline: Develop → Preview → Ship
- Each step has its own accent color: Blue → Pink → Red
- Connected with lines/arrows
- The visual metaphor for Vercel's core value proposition

**Trust Bar / Logo Grid**
- Company logos (Perplexity, ChatGPT, Cursor, etc.) in grayscale
- Horizontal scroll or grid layout
- Subtle `#ebebeb` border separation

**Metric Cards**
- Large number display (e.g., "10x faster")
- Geist 48px weight 600 for the metric
- Description below in gray body text
- Shadow-bordered card container

## 5. Layout Principles

### Spacing System
- Base unit: 8px
- Scale: 1px, 2px, 3px, 4px, 5px, 6px, 8px, 10px, 12px, 14px, 16px, 32px, 36px, 40px
- Notable gap: jumps from 16px to 32px — no 20px or 24px in primary scale. This is intentional: the leap enforces a binary decision between "component spacing" (16px and below) and "section spacing" (32px and above). Do not interpolate — if 16px feels too tight and 32px too loose, reconsider the component grouping rather than inventing a 24px value.
- **Interpolation rule**: Use only defined scale values. The spacing scale is a closed set — no ad-hoc values between steps.

### Grid & Container
- Max content width: approximately 1200px
- Hero: centered single-column with generous top padding
- Feature sections: 2–3 column grids for cards
- Full-width dividers using `border-bottom: 1px solid #171717`
- Code/dashboard screenshots as full-width or contained with border

### Whitespace Philosophy
- **Gallery emptiness**: Massive vertical padding between sections (80px–120px+). The white space IS the design — it communicates that Vercel has nothing to prove and nothing to hide.
- **Compressed text, expanded space**: The aggressive negative letter-spacing on headlines is counterbalanced by generous surrounding whitespace. The text is dense; the space around it is vast.
- **Section rhythm**: White sections alternate with white sections — there's no color variation between sections. Separation comes from borders (shadow-borders) and spacing alone.

### Density Modes

Vercel's design operates at two density levels depending on content type:

| Mode | Vertical Padding | Grid Gap | Use Case |
|------|-----------------|----------|----------|
| Marketing (Default) | 80–120px between sections | 32–40px | Landing pages, hero sections, feature showcases |
| Product / Data | 16–24px between sections | 8–16px | Dashboards, deployment logs, settings panels, data tables |

When building marketing pages, use the generous gallery spacing documented above. When building product interfaces (dashboards, settings, logs), compress to the tighter scale — the same 8px base unit, but the section gaps shrink from 80px+ to 16–24px. Cards in product contexts use 16px internal padding instead of 24–32px.

**Content-type density rule**: If the primary content is text and imagery (marketing), use wide spacing. If the primary content is data, controls, or status indicators (product), use tight spacing. Never mix densities within a single view.

### Border Radius Scale
- Micro (2px): Inline code snippets, small spans
- Subtle (4px): Small containers
- Standard (6px): Buttons, links, functional elements
- Comfortable (8px): Cards, list items
- Image (12px): Featured cards, image containers (top-rounded)
- Large (64px): Tab navigation pills
- XL (100px): Large navigation links
- Full Pill (9999px): Badges, status pills, tags
- Circle (50%): Menu toggle, avatar containers

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Flat (Level 0) | No shadow | Page background, text blocks |
| Ring (Level 1) | `rgba(0,0,0,0.08) 0px 0px 0px 1px` | Shadow-as-border for most elements |
| Light Ring (Level 1b) | `rgb(235,235,235) 0px 0px 0px 1px` | Lighter ring for tabs, images |
| Subtle Card (Level 2) | Ring + `rgba(0,0,0,0.04) 0px 2px 2px` | Standard cards with minimal lift |
| Full Card (Level 3) | Ring + Subtle + `rgba(0,0,0,0.04) 0px 8px 8px -8px` + inner `#fafafa` ring | Featured cards, highlighted panels |
| Focus (Accessibility) | `2px solid hsla(212, 100%, 48%, 1)` outline | Keyboard focus on all interactive elements |

**Shadow Philosophy**: Vercel has arguably the most sophisticated shadow system in modern web design. Rather than using shadows for elevation in the traditional Material Design sense, Vercel uses multi-value shadow stacks where each layer has a distinct architectural purpose: one creates the "border" (0px spread, 1px), another adds ambient softness (2px blur), another handles depth at distance (8px blur with negative spread), and an inner ring (`#fafafa`) creates the subtle highlight that makes the card "glow" from within. This layered approach means cards feel built, not floating.

### Decorative Depth
- Hero gradient: soft, pastel multi-color gradient wash behind hero content (barely visible, atmospheric)
- Section borders: `1px solid #171717` (full dark line) between major sections
- No background color variation — depth comes entirely from shadow layering and border contrast

## 7. Accessibility

Vercel's monochrome palette and engineering-first philosophy extend naturally to accessibility. The design system's high-contrast defaults and structured component patterns provide a strong baseline, but explicit accessibility rules ensure nothing is left to assumption.

### WCAG Target

The target compliance level is **WCAG 2.2 AA**. All text, interactive elements, and visual indicators must meet or exceed AA requirements. Where the existing palette already achieves AAA, that level should be preserved — do not regress to merely passing AA.

### Color Contrast Ratios

The achromatic palette produces the following contrast ratios against the white (`#ffffff`) background:

| Foreground | Hex | Contrast Ratio | WCAG AA Normal Text (4.5:1) | WCAG AA Large Text (3:1) | WCAG AAA Normal Text (7:1) |
|------------|-----|---------------|----------------------------|--------------------------|---------------------------|
| Vercel Black | `#171717` | ~17.4:1 | PASS | PASS | PASS (AAA) |
| Gray 600 | `#4d4d4d` | ~7.4:1 | PASS | PASS | PASS (AAA) |
| Gray 500 | `#666666` | ~5.7:1 | PASS | PASS | FAIL |
| Gray 400 | `#808080` | ~3.9:1 | **FAIL** | PASS | FAIL |

**Guidance**: `#808080` (Gray 400) must not be used for normal-sized text on white backgrounds. Restrict its use to placeholder text inside inputs (which is not required to meet contrast), disabled states (which are exempt from contrast requirements under WCAG), and large text (18px+ regular or 14px+ bold) where the 3:1 ratio is sufficient. All body copy, labels, and interactive text must use `#666666` or darker.

### Focus System

Every interactive element — buttons, links, inputs, toggles, cards with click handlers — must display a visible focus indicator on keyboard navigation:

- **Outline**: `2px solid hsla(212, 100%, 48%, 1)` (`--ds-focus-color`)
- **Outline offset**: `2px` (ensures the ring does not overlap the element's border/shadow)
- **Visibility**: The focus ring must be visible on both light (`#ffffff`) and dark (`#171717`) backgrounds. The saturated blue at `hsla(212, 100%, 48%, 1)` achieves sufficient contrast against both.
- **Never suppress**: Do not set `outline: none` without providing an equivalent or better custom focus indicator. The `:focus-visible` pseudo-class should be used to show focus rings only on keyboard interaction, hiding them on mouse clicks.

### ARIA Patterns

Key components must carry the following ARIA roles and attributes:

| Component | Role / Attribute | Notes |
|-----------|-----------------|-------|
| Buttons | `role="button"` (implicit on `<button>`) | Icon-only buttons require `aria-label` describing the action |
| Navigation | `role="navigation"`, `aria-label="Main navigation"` | Each distinct nav region needs a unique `aria-label` |
| Cards | `<article>` or `<section>` with `aria-labelledby` pointing to the card title | If the card is clickable, the entire card surface must be the click target, not a hidden anchor |
| Modals | `role="dialog"`, `aria-modal="true"` | Must also include `aria-labelledby` referencing the modal title and `aria-describedby` for body content |
| Badges | `role="status"` | Ensures screen readers announce badge content as a live status update |

### Motion Policy

All transitions, transforms, and animated shadows must respect the user's motion preference:

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    transition-duration: 0.01ms !important;
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transform: none !important;
  }
}
```

This disables hover scale transforms (e.g., `scale(1.02)` on cards), shadow transition animations, skeleton shimmer effects, and any decorative motion. Setting duration to `0.01ms` rather than `0` ensures `transitionend` events still fire for JavaScript listeners that depend on them.

### Minimum Touch Targets

Per WCAG 2.5.8 (Target Size), all interactive elements must meet minimum touch target dimensions:

- **Mobile**: 44x44px minimum tap area for all interactive elements. If the visible element is smaller (e.g., a 36px-tall button), invisible padding must extend the tap target to 44px.
- **Desktop buttons**: Minimum height of 36px. The primary dark button (8px 16px padding on ~14px text) naturally meets this. Compact buttons with 0px 6px padding must ensure the computed height reaches 36px.
- **Navigation links**: Minimum 44px tap area including padding. At 14px font size with adequate line-height and padding, nav links should compute to at least 44px of tappable space on touch devices.
- **Pill badges**: The 0px 10px horizontal padding on 12px text produces a small target. When badges are interactive (clickable/tappable), extend padding or add invisible tap area to reach 44x44px.

### Screen Reader Guidance

- **Heading hierarchy**: Heading levels must be semantic and sequential — `h1` for the page title, `h2` for major sections, `h3` for subsections, and so on. The visual hierarchy (48px display, 40px section, 32px sub-heading) must map directly to `h1` > `h2` > `h3`. Never skip levels (e.g., jumping from `h2` to `h4`).
- **Image alt text**: All meaningful images require descriptive `alt` text that conveys the image's purpose, not just its appearance ("Dashboard showing deployment status" rather than "screenshot"). Decorative images — gradient backgrounds, purely atmospheric illustrations — must use `alt=""` and `aria-hidden="true"` to be invisible to screen readers.
- **Icon-only buttons**: Every button that displays only an icon (hamburger menu, close, search) must include an `aria-label` describing the action ("Open menu", "Close dialog", "Search").
- **Live regions**: Toast notifications and dynamically appearing error messages should use `aria-live="polite"` (or `aria-live="assertive"` for critical errors) so screen readers announce them without requiring the user to navigate to them.

## 8. Interaction Patterns

Vercel's interactions are precise and restrained — no bouncy animations, no playful overshoot. Every state change communicates function through the smallest possible visual shift. The interaction layer follows the same philosophy as the visual layer: nothing decorative, everything structural.

### State Machine

| State | Buttons | Cards | Inputs | Links | Nav Items |
|-------|---------|-------|--------|-------|-----------|
| **Default** | bg per variant, cursor: pointer | white bg, shadow stack, cursor: default | white bg, shadow-border, cursor: text | `#0072f5` text, underline, cursor: pointer | `#171717` text, weight 500, cursor: pointer |
| **Hover** | bg darkens (white→`#f5f5f5`, dark→`#333`), shadow intensifies | shadow opacity increases to `rgba(0,0,0,0.12)`, `transform: scale(1.01)` | shadow-border darkens to `rgba(0,0,0,0.15)` | color darkens to `#005bb5`, underline thickens | color stays, underline appears or weight shifts to 600 |
| **Active / Pressed** | bg `#e5e5e5` (white) or `#444` (dark), `transform: scale(0.98)` | `transform: scale(0.99)`, shadow reduces | inner shadow `inset 0 1px 2px rgba(0,0,0,0.06)` | color `#004494` | weight 600, underline solid |
| **Focus** | `2px solid hsla(212,100%,48%,1)` outline, 2px offset | `2px solid hsla(212,100%,48%,1)` outline, 2px offset | `2px solid hsla(212,100%,48%,1)` outline, border-shadow intensifies | `2px solid hsla(212,100%,48%,1)` outline, 2px offset | `2px solid hsla(212,100%,48%,1)` outline, 2px offset |
| **Disabled** | bg `#fafafa`, text `#808080`, cursor: not-allowed, opacity: 0.6 | opacity: 0.5, pointer-events: none | bg `#fafafa`, text `#808080`, cursor: not-allowed | color `#808080`, no underline, cursor: default | color `#808080`, cursor: default |
| **Loading** | spinner replaces text, maintain width, cursor: wait | skeleton shimmer overlay, pointer-events: none | N/A | N/A | N/A |

### Transitions

All state transitions use consistent, minimal timing:

- **Color and background changes**: `150ms ease` — fast enough to feel instant, slow enough to not flash.
- **Shadow and transform changes**: `200ms ease` — slightly slower to give physical-feeling depth shifts time to register.
- **Default shorthand**: `transition: background 150ms ease, color 150ms ease, box-shadow 200ms ease, transform 200ms ease`
- **Reduced motion**: All transitions collapse to `0.01ms` duration when `prefers-reduced-motion: reduce` is active. See Section 7 Motion Policy.

### Modals & Overlays

- **Backdrop**: `hsla(0, 0%, 98%, 1)` (`--ds-overlay-backdrop-color`) — the near-white overlay rather than a dark scrim. This is distinctly Vercel: modals emerge from the white, not from darkness.
- **Focus trap**: When a modal is open, Tab and Shift+Tab must cycle only through focusable elements within the modal. Focus must not escape to the page behind.
- **Escape key**: Pressing Escape must close the modal. This is non-negotiable.
- **Scroll lock**: Apply `overflow: hidden` to `<body>` when a modal is open to prevent background scrolling.
- **Focus return**: On close, focus must return to the element that triggered the modal (the button that opened it). This maintains keyboard navigation context.
- **Animation**: Modals fade in with `opacity 200ms ease` and optionally `transform: translateY(4px)` to `translateY(0)`. Respect `prefers-reduced-motion`.

### Error States

- **Inline validation**: Error text appears directly below the offending input in red (`#e00`), at 12px Geist weight 400. The input's shadow-border shifts to a red ring: `0px 0px 0px 1px rgba(224, 0, 0, 0.4)`.
- **Error border**: Replaces the standard `rgba(0,0,0,0.08)` shadow-border with `rgba(224, 0, 0, 0.4) 0px 0px 0px 1px` — same technique, different color.
- **Form-level errors**: For errors that don't map to a single input (submission failures, server errors), use a toast notification or a banner at the top of the form. Toasts use the shadow-bordered card treatment with a red left-border accent.
- **Error icons**: Pair error text with a small icon (circle-exclamation) in the same red. Never rely on color alone — the icon and text together convey the error for color-blind users.

### Loading States

- **Skeleton screens**: Placeholder shapes matching the expected content layout, using `#fafafa` as the base color with an animated shimmer gradient (`linear-gradient(90deg, #fafafa 25%, #f0f0f0 50%, #fafafa 75%)`) that sweeps left to right. Background-size `200% 100%` with a `1.5s ease-in-out infinite` animation. Disable shimmer animation when `prefers-reduced-motion` is active — show static `#fafafa` blocks instead.
- **Button spinners**: When a button enters a loading state, replace the text content with a spinner (16px circular, `#171717` on light buttons, `#ffffff` on dark buttons). The button must maintain its exact width to prevent layout shift — set `min-width` to the button's computed width before loading begins.
- **Full-page loading**: Minimal — a thin progress bar at the top of the viewport (2px tall, `#171717`) or the Vercel triangle logo with a subtle pulse animation.

### Empty States

- **Layout**: Centered vertically and horizontally within the container. Text uses `#666666` (Gray 500), Geist 16px weight 400, with relaxed line-height (1.50–1.80).
- **Illustration**: Optional — a simple line illustration or icon in `#ebebeb` (Gray 100), communicating the empty state's context (empty inbox, no deployments, no results).
- **Call to action**: A single primary button (dark, `#171717`) below the explanatory text, offering the obvious next step ("Create your first project", "Add a domain"). Do not show multiple CTAs in empty states — clarity over choice.

## 9. Responsive Behavior

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile Small | <400px | Tight single column, minimal padding |
| Mobile | 400–600px | Standard mobile, stacked layout |
| Tablet Small | 600–768px | 2-column grids begin |
| Tablet | 768–1024px | Full card grids, expanded padding |
| Desktop Small | 1024–1200px | Standard desktop layout |
| Desktop | 1200–1400px | Full layout, maximum content width |
| Large Desktop | >1400px | Centered, generous margins |

### Touch Target Sizes

All interactive elements must meet explicit minimum dimensions rather than relying on vague "comfortable" padding:

- **Mobile interactive elements**: 44x44px minimum tap area per WCAG 2.5.8. This applies to buttons, links, toggles, checkboxes, and any other tappable element. If the visible element is smaller, extend the tap target with invisible padding or pseudo-elements.
- **Desktop buttons**: Minimum height of 36px. The primary dark button (`8px 16px` padding on 14px text) computes to approximately 38px — compliant. The compact white button (`0px 6px` padding) must ensure its line-height and min-height reach 36px.
- **Navigation links**: On touch devices, each nav link must provide at least 44px of tappable height. At 14px font size, this means a minimum of `14px 0` vertical padding on each link, or equivalent spacing between stacked items.
- **Pill badges**: When interactive, pill badges (12px text, 0px 10px padding) are naturally too small. Extend tap area to 44x44px minimum using padding or `::after` pseudo-elements with absolute positioning.
- **Mobile menu toggle**: The circular hamburger button (50% radius) must be at least 44x44px.

### Fluid Typography

Display and heading sizes use `clamp()` for smooth scaling between breakpoints, eliminating the need for per-breakpoint font-size overrides:

- **Display Hero**: `font-size: clamp(2rem, 5vw, 3rem)` — scales from 32px at narrow viewports to 48px at desktop. Letter-spacing should scale proportionally: `letter-spacing: clamp(-1.6px, -0.05em, -2.4px)`.
- **Section Heading**: `font-size: clamp(1.5rem, 4vw, 2.5rem)` — scales from 24px to 40px. Maintains the compressed Geist identity at all sizes.
- **Body text**: Stays fixed at 16px–18px. Body text does not benefit from fluid sizing — readability requires consistent sizing, and the 16px–18px range is already optimized for all viewports.

### Dark Mode Tokens

Vercel's dark mode inverts the canvas philosophy — from white gallery to black void. The same restraint applies: no decorative color, no gratuitous contrast shifts. Dark mode tokens map directly to their light-mode counterparts:

| Token | Light Mode | Dark Mode |
|-------|-----------|-----------|
| Background | `#ffffff` | `#000000` |
| Primary text | `#171717` | `#ededed` |
| Secondary text | `#4d4d4d` | `#888888` |
| Borders (shadow-border) | `rgba(0,0,0,0.08)` | `rgba(255,255,255,0.1)` |
| Card surface | `#ffffff` | `#111111` |
| Subtle surface | `#fafafa` | `#0a0a0a` |
| Disabled text | `#808080` | `#555555` |

**Shadow technique in dark mode**: The signature shadow-as-border shifts from `rgba(0,0,0,0.08) 0px 0px 0px 1px` to `rgba(255,255,255,0.1) 0px 0px 0px 1px`. Elevation shadows become impractical on dark backgrounds (dark shadow on dark surface is invisible), so dark mode relies more heavily on the border-shadow technique and subtle surface color differentiation (`#111111` cards on `#000000` background) rather than shadow-based depth. Where additional depth is needed, use `rgba(0,0,0,0.5) 0px 0px 0px 1px` — a heavier shadow that reads as a recessed border on dark surfaces.

**Dark Mode Interactive States**

| State | Property | Light Mode | Dark Mode |
|-------|----------|------------|-----------|
| Button hover | Background | `var(--ds-gray-1000)` | `#333333` |
| Card hover | Shadow opacity | 0.08 base | 0.15 base |
| Link hover | Color | `#0072f5` | `#4da3ff` |
| Input focus | Border | `hsla(212, 100%, 48%, 1)` | `hsla(212, 100%, 60%, 1)` |
| Nav active | Background | `#fafafa` | `#1a1a1a` |

### Container Queries

Card components should use container queries where supported, allowing cards to adapt their internal layout based on their own container width rather than the viewport:

```css
.card-container {
  container-type: inline-size;
}

@container (min-width: 400px) {
  .card {
    /* Switch from stacked to horizontal layout */
    flex-direction: row;
    gap: 16px;
  }
  .card-image {
    width: 40%;
    border-radius: 12px 0 0 12px;
  }
}
```

This is particularly valuable for Vercel's card grids, where the same card component may appear in a 3-column layout (narrow container) or a full-width featured slot (wide container). Container queries allow the card to respond to its actual available space, not the viewport width.

### Collapsing Strategy
- Hero: display 48px → scales down, maintains negative tracking proportionally
- Navigation: horizontal links + CTAs → hamburger menu
- Feature cards: 3-column → 2-column → single column stacked
- Code screenshots: maintain aspect ratio, may horizontally scroll
- Trust bar logos: grid → horizontal scroll
- Footer: multi-column → stacked single column
- Section spacing: 80px+ → 48px on mobile

### Image Behavior
- Dashboard screenshots maintain border treatment at all sizes
- Hero gradient softens/simplifies on mobile
- Product screenshots use responsive images with consistent border radius
- Full-width sections maintain edge-to-edge treatment

## 10. Do's and Don'ts

### Do
- Use Geist Sans with aggressive negative letter-spacing at display sizes (-2.4px to -2.88px at 48px)
- Use shadow-as-border (`0px 0px 0px 1px rgba(0,0,0,0.08)`) instead of traditional CSS borders
- Enable `"liga"` on all Geist text — ligatures are structural, not optional
- Use the three-weight system: 400 (body), 500 (UI), 600 (headings)
- Apply workflow accent colors (Red/Pink/Blue) only in their workflow context
- Use multi-layer shadow stacks for cards (border + elevation + ambient + inner highlight)
- Keep the color palette achromatic — grays from `#171717` to `#ffffff` are the system
- Use `#171717` instead of `#000000` for primary text — the micro-warmth matters

### Don't
- Don't use positive letter-spacing on Geist Sans — it's always negative or zero
- Don't use weight 700 (bold) on body text — 600 is the maximum, used only for headings
- Don't use traditional CSS `border` on cards — use the shadow-border technique
- Don't introduce warm colors (oranges, yellows, greens) into the UI chrome
- Don't apply the workflow accent colors (Ship Red, Preview Pink, Develop Blue) decoratively
- Don't use heavy shadows (> 0.1 opacity) — the shadow system is whisper-level
- Don't increase body text letter-spacing — Geist is designed to run tight
- Don't use pill radius (9999px) on primary action buttons — pills are for badges/tags only
- Don't skip the inner `#fafafa` ring in card shadows — it's the glow that makes the system work

## 11. Agent Prompt Guide

### Quick Color Reference
- Primary CTA: Vercel Black (`#171717`)
- Background: Pure White (`#ffffff`)
- Heading text: Vercel Black (`#171717`)
- Body text: Gray 600 (`#4d4d4d`)
- Border (shadow): `rgba(0, 0, 0, 0.08) 0px 0px 0px 1px`
- Link: Link Blue (`#0072f5`)
- Focus ring: Focus Blue (`hsla(212, 100%, 48%, 1)`)

### Example Component Prompts
- "Create a hero section on white background. Headline at 48px Geist weight 600, line-height 1.00, letter-spacing -2.4px, color #171717. Subtitle at 20px Geist weight 400, line-height 1.80, color #4d4d4d. Dark CTA button (#171717, 6px radius, 8px 16px padding) and ghost button (white, shadow-border rgba(0,0,0,0.08) 0px 0px 0px 1px, 6px radius)."
- "Design a card: white background, no CSS border. Use shadow stack: rgba(0,0,0,0.08) 0px 0px 0px 1px, rgba(0,0,0,0.04) 0px 2px 2px, #fafafa 0px 0px 0px 1px. Radius 8px. Title at 24px Geist weight 600, letter-spacing -0.96px. Body at 16px weight 400, #4d4d4d."
- "Build a pill badge: #ebf5ff background, #0068d6 text, 9999px radius, 0px 10px padding, 12px Geist weight 500."
- "Create navigation: white sticky header. Geist 14px weight 500 for links, #171717 text. Dark pill CTA 'Start Deploying' right-aligned. Shadow-border on bottom: rgba(0,0,0,0.08) 0px 0px 0px 1px."
- "Design a workflow section showing three steps: Develop (text color #0a72ef), Preview (#de1d8d), Ship (#ff5b4f). Each step: 14px Geist Mono uppercase label + 24px Geist weight 600 title + 16px weight 400 description in #4d4d4d."
- "Ensure all interactive elements have visible focus indicators (2px solid hsla(212, 100%, 48%, 1) outline), all images have alt text, heading hierarchy is semantic (h1 > h2 > h3), and color contrast meets WCAG AA (4.5:1 for normal text, 3:1 for large text)."

### Iteration Guide
1. Always use shadow-as-border instead of CSS border — `0px 0px 0px 1px rgba(0,0,0,0.08)` is the foundation
2. Letter-spacing scales with font size: -2.4px at 48px, -1.28px at 32px, -0.96px at 24px, normal at 14px
3. Three weights only: 400 (read), 500 (interact), 600 (announce)
4. Color is functional, never decorative — workflow colors (Red/Pink/Blue) mark pipeline stages only
5. The inner `#fafafa` ring in card shadows is what gives Vercel cards their subtle inner glow
6. Geist Mono uppercase for technical labels, Geist Sans for everything else
