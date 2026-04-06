# Design System Inspiration of Stripe

## 1. Visual Theme & Atmosphere

Stripe's website is the gold standard of fintech design -- a system that manages to feel simultaneously technical and luxurious, precise and warm. The page opens on a clean white canvas (`#ffffff`) with deep navy headings (`#061b31`) and a signature purple (`#533afd`) that functions as both brand anchor and interactive accent. This isn't the cold, clinical purple of enterprise software; it's a rich, saturated violet that reads as confident and premium. The overall impression is of a financial institution redesigned by a world-class type foundry.

The custom `sohne-var` variable font is the defining element of Stripe's visual identity. Every text element enables the OpenType `"ss01"` stylistic set, which modifies character shapes for a distinctly geometric, modern feel. At display sizes (48px-56px), sohne-var runs at weight 300 -- an extraordinarily light weight for headlines that creates an ethereal, almost whispered authority. This is the opposite of the "bold hero headline" convention; Stripe's headlines feel like they don't need to shout. The negative letter-spacing (-1.4px at 56px, -0.96px at 48px) tightens the text into dense, engineered blocks. At smaller sizes, the system also uses weight 300 with proportionally reduced tracking, and tabular numerals via `"tnum"` for financial data display.

What truly distinguishes Stripe is its shadow system. Rather than the flat or single-layer approach of most sites, Stripe uses multi-layer, blue-tinted shadows: the signature `rgba(50,50,93,0.25)` combined with `rgba(0,0,0,0.1)` creates shadows with a cool, almost atmospheric depth -- like elements are floating in a twilight sky. The blue-gray undertone of the primary shadow color (50,50,93) ties directly to the navy-purple brand palette, making even elevation feel on-brand.

**Key Characteristics:**
- sohne-var with OpenType `"ss01"` on all text -- a custom stylistic set that defines the brand's letterforms
- Weight 300 as the signature headline weight -- light, confident, anti-convention
- Negative letter-spacing at display sizes (-1.4px at 56px, progressive relaxation downward)
- Blue-tinted multi-layer shadows using `rgba(50,50,93,0.25)` -- elevation that feels brand-colored
- Deep navy (`#061b31`) headings instead of black -- warm, premium, financial-grade
- Conservative border-radius (4px-8px) -- nothing pill-shaped, nothing harsh
- Ruby (`#ea2261`) and magenta (`#f96bee`) accents for gradient and decorative elements
- `SourceCodePro` as the monospace companion for code and technical labels

## 2. Color Palette & Roles

### Primary
- **Stripe Purple** (`#533afd`): Primary brand color, CTA backgrounds, link text, interactive highlights. A saturated blue-violet that anchors the entire system.
- **Deep Navy** (`#061b31`): `--hds-color-heading-solid`. Primary heading color. Not black, not gray -- a very dark blue that adds warmth and depth to text.
- **Pure White** (`#ffffff`): Page background, card surfaces, button text on dark backgrounds.

### Brand & Dark
- **Brand Dark** (`#1c1e54`): `--hds-color-util-brand-900`. Deep indigo for dark sections, footer backgrounds, and immersive brand moments.
- **Dark Navy** (`#0d253d`): `--hds-color-core-neutral-975`. The darkest neutral -- almost-black with a blue undertone for maximum depth without harshness.

### Accent Colors
- **Ruby** (`#ea2261`): `--hds-color-accentColorMode-ruby-icon-solid`. Warm red-pink for icons, alerts, and accent elements.
- **Magenta** (`#f96bee`): `--hds-color-accentColorMode-magenta-icon-gradientMiddle`. Vivid pink-purple for gradients and decorative highlights.
- **Magenta Light** (`#ffd7ef`): `--hds-color-util-accent-magenta-100`. Tinted surface for magenta-themed cards and badges.

### Interactive
- **Primary Purple** (`#533afd`): Primary link color, active states, selected elements.
- **Purple Hover** (`#4434d4`): Darker purple for hover states on primary elements.
- **Purple Deep** (`#2e2b8c`): `--hds-color-button-ui-iconHover`. Dark purple for icon hover states.
- **Purple Light** (`#b9b9f9`): `--hds-color-action-bg-subduedHover`. Soft lavender for subdued hover backgrounds.
- **Purple Mid** (`#665efd`): `--hds-color-input-selector-text-range`. Range selector and input highlight color.

### Neutral Scale
- **Heading** (`#061b31`): Primary headings, nav text, strong labels.
- **Label** (`#273951`): `--hds-color-input-text-label`. Form labels, secondary headings.
- **Body** (`#64748d`): Secondary text, descriptions, captions.
- **Success Green** (`#15be53`): Status badges, success indicators (with 0.2-0.4 alpha for backgrounds/borders).
- **Success Text** (`#108c3d`): Success badge text color.
- **Lemon** (`#9b6829`): `--hds-color-core-lemon-500`. Warning and highlight accent.

### Surface & Borders
- **Border Default** (`#e5edf5`): Standard border color for cards, dividers, and containers.
- **Border Purple** (`#b9b9f9`): Active/selected state borders on buttons and inputs.
- **Border Soft Purple** (`#d6d9fc`): Subtle purple-tinted borders for secondary elements.
- **Border Magenta** (`#ffd7ef`): Pink-tinted borders for magenta-themed elements.
- **Border Dashed** (`#362baa`): Dashed borders for drop zones and placeholder elements.

### Shadow Colors
- **Shadow Blue** (`rgba(50,50,93,0.25)`): The signature -- blue-tinted primary shadow color.
- **Shadow Dark Blue** (`rgba(3,3,39,0.25)`): Deeper blue shadow for elevated elements.
- **Shadow Black** (`rgba(0,0,0,0.1)`): Secondary shadow layer for depth reinforcement.
- **Shadow Ambient** (`rgba(23,23,23,0.08)`): Soft ambient shadow for subtle elevation.
- **Shadow Soft** (`rgba(23,23,23,0.06)`): Minimal ambient shadow for light lift.

## 3. Typography Rules

### Font Family
- **Primary**: `sohne-var`, with fallback: `SF Pro Display`
- **Monospace**: `SourceCodePro`, with fallback: `SFMono-Regular`
- **OpenType Features**: `"ss01"` enabled globally on all sohne-var text; `"tnum"` for tabular numbers on financial data and captions.

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Features | Notes |
|------|------|------|--------|-------------|----------------|----------|-------|
| Display Hero | sohne-var | 56px (3.50rem) | 300 | 1.03 (tight) | -1.4px | ss01 | Maximum size, whisper-weight authority |
| Display Large | sohne-var | 48px (3.00rem) | 300 | 1.15 (tight) | -0.96px | ss01 | Secondary hero headlines |
| Section Heading | sohne-var | 32px (2.00rem) | 300 | 1.10 (tight) | -0.64px | ss01 | Feature section titles |
| Sub-heading Large | sohne-var | 26px (1.63rem) | 300 | 1.12 (tight) | -0.26px | ss01 | Card headings, sub-sections |
| Sub-heading | sohne-var | 22px (1.38rem) | 300 | 1.10 (tight) | -0.22px | ss01 | Smaller section heads |
| Body Large | sohne-var | 18px (1.13rem) | 300 | 1.40 | normal | ss01 | Feature descriptions, intro text |
| Body | sohne-var | 16px (1.00rem) | 300-400 | 1.40 | normal | ss01 | Standard reading text |
| Button | sohne-var | 16px (1.00rem) | 400 | 1.00 (tight) | normal | ss01 | Primary button text |
| Button Small | sohne-var | 14px (0.88rem) | 400 | 1.00 (tight) | normal | ss01 | Secondary/compact buttons |
| Link | sohne-var | 14px (0.88rem) | 400 | 1.00 (tight) | normal | ss01 | Navigation links |
| Caption | sohne-var | 13px (0.81rem) | 400 | normal | normal | ss01 | Small labels, metadata |
| Caption Small | sohne-var | 12px (0.75rem) | 300-400 | 1.33-1.45 | normal | ss01 | Fine print, timestamps |
| Caption Tabular | sohne-var | 12px (0.75rem) | 300-400 | 1.33 | -0.36px | tnum | Financial data, numbers |
| Micro | sohne-var | 10px (0.63rem) | 300 | 1.15 (tight) | 0.1px | ss01 | Tiny labels, axis markers |
| Micro Tabular | sohne-var | 10px (0.63rem) | 300 | 1.15 (tight) | -0.3px | tnum | Chart data, small numbers |
| Nano | sohne-var | 8px (0.50rem) | 300 | 1.07 (tight) | normal | ss01 | Smallest labels |
| Code Body | SourceCodePro | 12px (0.75rem) | 500 | 2.00 (relaxed) | normal | -- | Code blocks, syntax |
| Code Bold | SourceCodePro | 12px (0.75rem) | 700 | 2.00 (relaxed) | normal | -- | Bold code, keywords |
| Code Label | SourceCodePro | 12px (0.75rem) | 500 | 2.00 (relaxed) | normal | uppercase | Technical labels |
| Code Micro | SourceCodePro | 9px (0.56rem) | 500 | 1.00 (tight) | normal | ss01 | Tiny code annotations |

### Principles
- **Light weight as signature**: Weight 300 at display sizes is Stripe's most distinctive typographic choice. Where others use 600-700 to command attention, Stripe uses lightness as luxury -- the text is so confident it doesn't need weight to be authoritative.
- **ss01 everywhere**: The `"ss01"` stylistic set is non-negotiable. It modifies specific glyphs (likely alternate `a`, `g`, `l` forms) to create a more geometric, contemporary feel across all sohne-var text.
- **Two OpenType modes**: `"ss01"` for display/body text, `"tnum"` for tabular numerals in financial data. These never overlap -- a number in a paragraph uses ss01, a number in a data table uses tnum.
- **Progressive tracking**: Letter-spacing tightens proportionally with size: -1.4px at 56px, -0.96px at 48px, -0.64px at 32px, -0.26px at 26px, normal at 16px and below.
- **Two-weight simplicity**: Primarily 300 (body and headings) and 400 (UI/buttons). No bold (700) in the primary font -- SourceCodePro uses 500/700 for code contrast.

## 4. Component Stylings

### Buttons

**Primary Purple**
- Background: `#533afd`
- Text: `#ffffff`
- Padding: 8px 16px
- Radius: 4px
- Font: 16px sohne-var weight 400, `"ss01"`
- Hover: `#4434d4` background
- Use: Primary CTA ("Start now", "Contact sales")

**Ghost / Outlined**
- Background: transparent
- Text: `#533afd`
- Padding: 8px 16px
- Radius: 4px
- Border: `1px solid #b9b9f9`
- Font: 16px sohne-var weight 400, `"ss01"`
- Hover: background shifts to `rgba(83,58,253,0.05)`
- Use: Secondary actions

**Transparent Info**
- Background: transparent
- Text: `#2874ad`
- Padding: 8px 16px
- Radius: 4px
- Border: `1px solid rgba(43,145,223,0.2)`
- Use: Tertiary/info-level actions

**Neutral Ghost**
- Background: transparent (`rgba(255,255,255,0)`)
- Text: `rgba(16,16,16,0.3)`
- Padding: 8px 16px
- Radius: 4px
- Outline: `1px solid rgb(212,222,233)`
- Use: Disabled or muted actions

### Cards & Containers
- Background: `#ffffff`
- Border: `1px solid #e5edf5` (standard) or `1px solid #061b31` (dark accent)
- Radius: 4px (tight), 5px (standard), 6px (comfortable), 8px (featured)
- Shadow (standard): `rgba(50,50,93,0.25) 0px 30px 45px -30px, rgba(0,0,0,0.1) 0px 18px 36px -18px`
- Shadow (ambient): `rgba(23,23,23,0.08) 0px 15px 35px 0px`
- Hover: shadow intensifies, often adding the blue-tinted layer

### Badges / Tags / Pills
**Neutral Pill**
- Background: `#ffffff`
- Text: `#000000`
- Padding: 0px 6px
- Radius: 4px
- Border: `1px solid #f6f9fc`
- Font: 11px weight 400

**Success Badge**
- Background: `rgba(21,190,83,0.2)`
- Text: `#108c3d`
- Padding: 1px 6px
- Radius: 4px
- Border: `1px solid rgba(21,190,83,0.4)`
- Font: 10px weight 300

### Inputs & Forms
- Border: `1px solid #e5edf5`
- Radius: 4px
- Focus: `1px solid #533afd` or purple ring
- Label: `#273951`, 14px sohne-var
- Text: `#061b31`
- Placeholder: `#64748d`

### Navigation
- Clean horizontal nav on white, sticky with blur backdrop
- Brand logotype left-aligned
- Links: sohne-var 14px weight 400, `#061b31` text with `"ss01"`
- Radius: 6px on nav container
- CTA: purple button right-aligned ("Sign in", "Start now")
- Mobile: hamburger toggle with 6px radius

### Decorative Elements
**Dashed Borders**
- `1px dashed #362baa` (purple) for placeholder/drop zones
- `1px dashed #ffd7ef` (magenta) for magenta-themed decorative borders

**Gradient Accents**
- Ruby-to-magenta gradients (`#ea2261` to `#f96bee`) for hero decorations
- Brand dark sections use `#1c1e54` backgrounds with white text

## 5. Layout Principles

### Spacing System
- Base unit: 8px
- Scale: 1px, 2px, 4px, 6px, 8px, 10px, 11px, 12px, 14px, 16px, 18px, 20px
- Notable: The scale is dense at the small end (every 2px from 4-12), reflecting Stripe's precision-oriented UI for financial data

### Grid & Container
- Max content width: approximately 1080px
- Hero: centered single-column with generous padding, lightweight headlines
- Feature sections: 2-3 column grids for feature cards
- Full-width dark sections with `#1c1e54` background for brand immersion
- Code/dashboard previews as contained cards with blue-tinted shadows

### Whitespace Philosophy
- **Precision spacing**: Unlike the vast emptiness of minimalist systems, Stripe uses measured, purposeful whitespace. Every gap is a deliberate typographic choice.
- **Dense data, generous chrome**: Financial data displays (tables, charts) are tightly packed, but the UI chrome around them is generously spaced. This creates a sense of controlled density -- like a well-organized spreadsheet in a beautiful frame.
- **Section rhythm**: White sections alternate with dark brand sections (`#1c1e54`), creating a dramatic light/dark cadence that prevents monotony without introducing arbitrary color.

### Border Radius Scale
- Micro (1px): Fine-grained elements, subtle rounding
- Standard (4px): Buttons, inputs, badges, cards -- the workhorse
- Comfortable (5px): Standard card containers
- Relaxed (6px): Navigation, larger interactive elements
- Large (8px): Featured cards, hero elements
- Compound: `0px 0px 6px 6px` for bottom-rounded containers (tab panels, dropdown footers)

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Flat (Level 0) | No shadow | Page background, inline text |
| Ambient (Level 1) | `rgba(23,23,23,0.06) 0px 3px 6px` | Subtle card lift, hover hints |
| Standard (Level 2) | `rgba(23,23,23,0.08) 0px 15px 35px` | Standard cards, content panels |
| Elevated (Level 3) | `rgba(50,50,93,0.25) 0px 30px 45px -30px, rgba(0,0,0,0.1) 0px 18px 36px -18px` | Featured cards, dropdowns, popovers |
| Deep (Level 4) | `rgba(3,3,39,0.25) 0px 14px 21px -14px, rgba(0,0,0,0.1) 0px 8px 17px -8px` | Modals, floating panels |
| Ring (Accessibility) | `2px solid #533afd` outline | Keyboard focus ring |

**Shadow Philosophy**: Stripe's shadow system is built on a principle of chromatic depth. Where most design systems use neutral gray or black shadows, Stripe's primary shadow color (`rgba(50,50,93,0.25)`) is a deep blue-gray that echoes the brand's navy palette. This creates shadows that don't just add depth -- they add brand atmosphere. The multi-layer approach pairs this blue-tinted shadow with a pure black secondary layer (`rgba(0,0,0,0.1)`) at a different offset, creating a parallax-like depth where the branded shadow sits farther from the element and the neutral shadow sits closer. The negative spread values (-30px, -18px) ensure shadows don't extend beyond the element's footprint horizontally, keeping elevation vertical and controlled.

### Decorative Depth
- Dark brand sections (`#1c1e54`) create immersive depth through background color contrast
- Gradient overlays with ruby-to-magenta transitions for hero decorations
- Shadow color `rgba(0,55,112,0.08)` (`--hds-color-shadow-sm-top`) for top-edge shadows on sticky elements

## 7. Accessibility

Stripe handles money. Accessibility in financial interfaces is not a nice-to-have -- it is a regulatory expectation and an ethical baseline. Every element in this system must be perceivable, operable, and understandable to all users, including those navigating with screen readers, keyboards, or assistive devices.

### WCAG Target

**WCAG 2.2 AA** compliance across all components and pages. Financial services context demands particular rigor: users must be able to read balances, navigate dashboards, and complete transactions without visual dependence. Where AA is the floor, aim for AAA on critical financial data.

### Color Contrast Ratios

All text pairings have been evaluated against WCAG 2.2 luminance contrast requirements (4.5:1 for normal text, 3:1 for large text and UI components).

| Foreground | Background | Ratio | Rating | Use |
|------------|------------|-------|--------|-----|
| `#061b31` (Deep Navy) | `#ffffff` (White) | ~15.8:1 | AAA | Headings on white -- exceeds all thresholds |
| `#64748d` (Slate) | `#ffffff` (White) | ~4.8:1 | AA | Body text on white -- passes AA for normal text |
| `#273951` (Dark Slate) | `#ffffff` (White) | ~10.6:1 | AAA | Labels on white -- strong contrast |
| `#533afd` (Purple) | `#ffffff` (White) | ~5.2:1 | AA | Links and interactive text on white |
| `#ffffff` (White) | `#533afd` (Purple) | ~5.2:1 | AA | Button text on purple CTA backgrounds |
| `#ffffff` (White) | `#1c1e54` (Brand Dark) | ~14.3:1 | AAA | Text on dark brand sections -- excellent |
| `#108c3d` (Success Text) | `rgba(21,190,83,0.2)` | -- | Verify | Success badge text on green tint -- verify in context. The semi-transparent background composites differently on white vs. dark surfaces. Test the rendered composite. |

**Note on the success badge**: The pairing of `#108c3d` on `rgba(21,190,83,0.2)` composited over white produces an effective background of approximately `#d8f5e1`. This yields a contrast ratio of roughly 4.2:1 -- borderline AA for normal text at 10px. At that size, this text is classified as "incidental" under WCAG, but for financial status indicators, consider increasing font weight to 400 or size to 12px to improve legibility.

### Focus System

- **Ring**: `2px solid #533afd` outline on all interactive elements -- buttons, links, inputs, selects, checkboxes, cards with actions.
- **Offset**: `outline-offset: 2px` to prevent the ring from overlapping element borders.
- **Visibility on all surfaces**: The purple ring must be visible on white (`#ffffff`), brand dark (`#1c1e54`), and all card surface colors. On dark backgrounds, the purple ring maintains adequate contrast (~3.5:1 against `#1c1e54`). If needed, add a 1px white inner outline for reinforcement on very dark surfaces.
- **Consistency**: Every focusable element uses the same ring. No exceptions, no per-component overrides.
- **`:focus-visible` only**: Apply focus ring on keyboard navigation, not mouse clicks. Use `:focus-visible` to keep the interface clean for pointer users while remaining fully accessible for keyboard users.

### ARIA Patterns

| Element | Role/Attribute | Implementation |
|---------|---------------|----------------|
| Buttons | `role="button"` | Native `<button>` preferred. Custom elements require `role="button"`, `tabindex="0"`, and keydown handlers for Enter and Space. |
| Navigation | `role="navigation"` | Wrap with `<nav aria-label="Main navigation">`. Multiple nav regions require distinct `aria-label` values. |
| Financial data tables | `role="table"` | Use semantic `<table>`, `<th scope="col">`, `<th scope="row">`. Complex tables require `aria-describedby` linking to a caption that explains the data. |
| Form inputs | `aria-required`, `aria-describedby` | Required fields use `aria-required="true"`. Error messages linked via `aria-describedby`. Labels linked via `for`/`id` or wrapping `<label>`. |
| Success/error badges | `role="status"` | Live regions with `role="status"` and `aria-live="polite"` so screen readers announce state changes without interrupting. |
| Modals | `role="dialog"`, `aria-modal="true"` | Focus trapped within modal. First focusable element receives focus on open. Escape closes. `aria-labelledby` links to modal heading. |

### Motion Policy

```css
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    transition-duration: 0.01ms !important;
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
  }
}
```

- All hover shadow transitions, button state changes, and gradient animations are disabled under `prefers-reduced-motion: reduce`.
- Financial dashboards -- where users are reading numbers and making decisions -- should avoid decorative motion entirely, regardless of user preference. Data updates should appear instantly, not animate in.
- Loading spinners are exempt (they communicate system state), but skeleton shimmers should stop.

### Minimum Touch Targets

- **Mobile**: 44x44px minimum on all interactive elements (WCAG 2.2 Target Size).
- **Desktop**: 36px minimum height on buttons and interactive controls.
- **Small elements**: Badge elements at 10px text with `1px 6px` padding are visually small by design. Extend the tappable area to 44px using transparent padding or `::after` pseudo-element hit areas. The visual footprint remains compact; the touch target does not.

### Screen Reader Guidance

- **Financial values**: Use `aria-label` to provide semantic context. A cell displaying "$4,200" should read as `aria-label="$4,200 return on investment"` or `aria-label="Balance: $4,200"` -- not just the raw number. Currency, context, and meaning must be explicit.
- **Tables**: Every data table requires proper `<th>` headers with `scope`. Summary rows should use `aria-label` to describe the aggregation ("Total revenue: $42,000").
- **Code blocks**: Wrap in `<pre>` with `aria-label` describing the code's purpose ("Example: creating a PaymentIntent with the Stripe API"), not its content line by line.
- **Icons and decorative elements**: Decorative icons use `aria-hidden="true"`. Functional icons (close, menu, expand) require `aria-label`.
- **Status badges**: "Active", "Succeeded", "Failed" badges must be announced with context: `aria-label="Payment status: Succeeded"`.

## 8. Interaction Patterns

Stripe's interactions are understated and precise -- state changes happen quickly, feel mechanical rather than playful, and never distract from financial data. Every transition serves a functional purpose: confirming a hover, acknowledging a click, signaling that the system is working.

### State Machine

| Component | Default | Hover | Active | Focus | Disabled | Loading |
|-----------|---------|-------|--------|-------|----------|---------|
| **Button (Primary Purple)** | `bg: #533afd` `text: #fff` | `bg: #4434d4` | `bg: #2e2b8c` `transform: scale(0.98)` | `outline: 2px solid #533afd` `outline-offset: 2px` | `bg: #533afd` `opacity: 0.4` `cursor: not-allowed` | `bg: #533afd` spinner replaces text, width maintained |
| **Button (Ghost)** | `bg: transparent` `border: 1px solid #b9b9f9` `text: #533afd` | `bg: rgba(83,58,253,0.05)` | `bg: rgba(83,58,253,0.1)` | `outline: 2px solid #533afd` `outline-offset: 2px` | `opacity: 0.4` `cursor: not-allowed` | Spinner in `#533afd`, width maintained |
| **Button (Neutral)** | `bg: transparent` `outline: 1px solid rgb(212,222,233)` `text: rgba(16,16,16,0.3)` | `border-color: #b9b9f9` `text: #273951` | `bg: rgba(0,0,0,0.03)` | `outline: 2px solid #533afd` `outline-offset: 2px` | `opacity: 0.3` `cursor: not-allowed` | -- |
| **Card** | `shadow: Level 2` `border: 1px solid #e5edf5` | `shadow: Level 3` | -- | `outline: 2px solid #533afd` (if interactive) | `opacity: 0.6` | Skeleton shimmer fills content area |
| **Input** | `border: 1px solid #e5edf5` `text: #061b31` | `border-color: #b9b9f9` | `border-color: #533afd` | `outline: 2px solid #533afd` `outline-offset: 0` | `bg: #f6f9fc` `opacity: 0.5` `cursor: not-allowed` | -- |
| **Link** | `text: #533afd` `text-decoration: none` | `text-decoration: underline` | `text: #2e2b8c` | `outline: 2px solid #533afd` `outline-offset: 2px` | `text: #64748d` `cursor: not-allowed` | -- |
| **Badge** | Per badge type (see Section 4) | -- | -- | -- | `opacity: 0.4` | -- |

### Transitions

- **Background color**: `transition: background-color 200ms ease`
- **Border color**: `transition: border-color 200ms ease`
- **Box shadow**: `transition: box-shadow 300ms ease` -- longer duration because Stripe's blue-tinted, multi-layer shadows are atmospheric. A fast shadow transition looks mechanical; 300ms lets the depth shift feel natural.
- **Transform**: `transition: transform 100ms ease` -- button press feedback should be instantaneous.
- **Opacity**: `transition: opacity 200ms ease`
- **Combined**: `transition: background-color 200ms ease, box-shadow 300ms ease, border-color 200ms ease, transform 100ms ease`
- All transitions respect `prefers-reduced-motion` (see Section 7, Motion Policy).

### Modals & Overlays

- **Backdrop**: `rgba(6,27,49,0.6)` -- navy-tinted, not neutral gray. The overlay is on-brand, casting the page in the same deep blue tone as the brand dark palette.
- **Focus trap**: On open, focus moves to the first focusable element inside the modal. Tab cycles within the modal. Shift+Tab cycles in reverse. Focus never escapes to the page behind.
- **Escape closes**: Pressing Escape dismisses the modal and returns focus to the trigger element.
- **Scroll lock**: `body { overflow: hidden }` while modal is open. Prevent background scroll on both desktop and mobile (use `touch-action: none` on the backdrop for iOS).
- **Animation**: Modal fades in with `opacity 200ms ease` and subtle `translateY(-8px)` to `translateY(0)`. Backdrop fades in at `opacity 300ms ease`. Both disabled under `prefers-reduced-motion`.

### Error States

- **Inline validation**: Error text in Ruby (`#ea2261`), 13px sohne-var weight 400 with `"ss01"`. Appears below the input, linked via `aria-describedby`.
- **Input border**: Shifts from default `#e5edf5` to `#ea2261` on error. Transition: `border-color 200ms ease`.
- **Form-level errors**: Banner pattern -- full-width bar above the form with Ruby background at `rgba(234,34,97,0.08)`, Ruby left border (3px solid `#ea2261`), error text in `#ea2261`, and a close/dismiss action. Announced via `aria-live="assertive"`.
- **Error icons**: 16px, `#ea2261` fill, placed inline-start of error text. Use `aria-hidden="true"` (the text carries the message).

### Loading States

- **Skeleton screens**: Card content areas replaced with placeholder blocks. Background: `#e5edf5` with a shimmer animation -- a subtle purple-tinted gradient (`#e5edf5` through `rgba(83,58,253,0.03)` back to `#e5edf5`) sweeping left to right over 1.5s, infinite loop. Disabled under `prefers-reduced-motion` (static `#e5edf5` block instead).
- **Button loading**: Text replaced with a 16px spinner (2px stroke, `#ffffff` on primary buttons, `#533afd` on ghost buttons). Button width locked via `min-width` matching its resting state to prevent layout shift. Button remains non-interactive (`pointer-events: none`, `aria-disabled="true"`).
- **Page/section loading**: Skeleton fills the content area with placeholder blocks matching the expected layout shape -- heading block, body text lines, card outlines. This maintains spatial stability.

### Empty States

- **Heading**: Deep navy (`#061b31`), 22px sohne-var weight 300, letter-spacing -0.22px, `"ss01"`. Clear, human statement of the empty condition ("No transactions yet").
- **Body text**: Slate (`#64748d`), 16px weight 300. Brief guidance on what to do next.
- **CTA**: Purple primary button (`#533afd`) guiding the user to the action that populates the empty state ("Create your first product", "Connect a bank account").
- **Illustration** (optional): Muted, brand-tinted line art. Never clip art. Keep it geometric and consistent with Stripe's engineering-forward aesthetic.

## 9. Responsive Behavior

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | <640px | Single column, reduced heading sizes, stacked cards |
| Tablet | 640-1024px | 2-column grids, moderate padding |
| Desktop | 1024-1280px | Full layout, 3-column feature grids |
| Large Desktop | >1280px | Centered content with generous margins |

### Fluid Typography

Rather than hard breakpoint steps, display type scales fluidly using `clamp()` to maintain Stripe's typographic precision across every viewport width.

| Role | Fluid Rule | Notes |
|------|-----------|-------|
| Display Hero/Large | `font-size: clamp(2rem, 4.5vw, 3.5rem)` | Scales from 32px to 56px. Weight 300 maintained at all sizes -- the light weight is resolution-independent. |
| Section Heading | `font-size: clamp(1.5rem, 3vw, 2rem)` | Scales from 24px to 32px. Letter-spacing should also interpolate (tighter at larger sizes). |
| Body/UI | Fixed at `1rem` / `0.875rem` | Body text does not scale fluidly. Readability requires stable sizing. |

Letter-spacing adjusts proportionally: at the `clamp()` minimum, use the smaller size's tracking value; at the maximum, use the larger size's tracking.

### Dark Mode Tokens

Stripe already uses `#1c1e54` for dark brand sections. A full dark mode extends this palette across the entire interface.

| Token | Light Mode | Dark Mode |
|-------|-----------|-----------|
| `--background` | `#ffffff` | `#0a0a1a` |
| `--text-heading` | `#061b31` | `#e8e8f0` |
| `--text-body` | `#64748d` | `#a0a0b8` |
| `--border` | `#e5edf5` | `rgba(255,255,255,0.08)` |
| `--card-surface` | `#ffffff` | `#1c1e54` |
| `--shadow-primary` | `rgba(50,50,93,0.25)` | `rgba(0,0,0,0.4)` |
| `--shadow-secondary` | `rgba(0,0,0,0.1)` | `rgba(3,3,39,0.3)` |
| `--shadow-ambient` | `rgba(23,23,23,0.08)` | `rgba(0,0,0,0.3)` |

**Dark mode philosophy**: The dark palette is not an inversion -- it's an extension of the brand dark sections. `#0a0a1a` is deeper than `#1c1e54`, creating a hierarchy where cards (`#1c1e54`) float above the page background. Shadows shift to near-black with a deep blue undertone, maintaining the chromatic depth principle. The purple accent (`#533afd`) remains unchanged -- it has sufficient contrast on both light and dark surfaces.

### Container Queries

Card components adapt their internal layout based on available space rather than viewport width. This ensures cards render correctly whether placed in a single-column mobile layout, a sidebar, or a multi-column desktop grid.

```css
.card-container {
  container-type: inline-size;
}

@container (min-width: 350px) {
  .card-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }
}

@container (max-width: 349px) {
  .card-content {
    display: flex;
    flex-direction: column;
    gap: 12px;
  }
}
```

### Touch Target Sizes

- **Buttons**: All buttons enforce a minimum 44x44px touch target on mobile via `min-height: 44px; min-width: 44px`. Padding increases if needed to meet the threshold.
- **Badges**: Badge elements are visually compact (10px text, `1px 6px` padding) but wrapped in a tappable area padded to 44px using a transparent `::after` pseudo-element:
  ```css
  .badge {
    position: relative;
  }
  .badge::after {
    content: '';
    position: absolute;
    inset: -12px -8px; /* expand to ~44px touch target */
    /* transparent, no visual change */
  }
  ```
- **Links in navigation**: Minimum 44px tappable height on mobile, achieved via padding rather than increased font size.

### Collapsing Strategy
- Hero: 56px display -> 32px on mobile, weight 300 maintained
- Navigation: horizontal links + CTAs -> hamburger toggle
- Feature cards: 3-column -> 2-column -> single column stacked
- Dark brand sections: maintain full-width treatment, reduce internal padding
- Financial data tables: horizontal scroll on mobile
- Section spacing: 64px+ -> 40px on mobile
- Typography scale compresses: 56px -> 48px -> 32px hero sizes across breakpoints

### Image Behavior
- Dashboard/product screenshots maintain blue-tinted shadow at all sizes
- Hero gradient decorations simplify on mobile
- Code blocks maintain `SourceCodePro` treatment, may horizontally scroll
- Card images maintain consistent 4px-6px border-radius

## 10. Do's and Don'ts

### Do
- Use sohne-var with `"ss01"` on every text element -- the stylistic set IS the brand
- Use weight 300 for all headlines and body text -- lightness is the signature
- Apply blue-tinted shadows (`rgba(50,50,93,0.25)`) for all elevated elements
- Use `#061b31` (deep navy) for headings instead of `#000000` -- the warmth matters
- Keep border-radius between 4px-8px -- conservative rounding is intentional
- Use `"tnum"` for any tabular/financial number display
- Layer shadows: blue-tinted far + neutral close for depth parallax
- Use `#533afd` purple as the primary interactive/CTA color

### Don't
- Don't use weight 600-700 for sohne-var headlines -- weight 300 is the brand voice
- Don't use large border-radius (12px+, pill shapes) on cards or buttons -- Stripe is conservative
- Don't use neutral gray shadows -- always tint with blue (`rgba(50,50,93,...)`)
- Don't skip `"ss01"` on any sohne-var text -- the alternate glyphs define the personality
- Don't use pure black (`#000000`) for headings -- always `#061b31` deep navy
- Don't use warm accent colors (orange, yellow) for interactive elements -- purple is primary
- Don't apply positive letter-spacing at display sizes -- Stripe tracks tight
- Don't use the magenta/ruby accents for buttons or links -- they're decorative/gradient only

## 11. Agent Prompt Guide

### Quick Color Reference
- Primary CTA: Stripe Purple (`#533afd`)
- CTA Hover: Purple Dark (`#4434d4`)
- Background: Pure White (`#ffffff`)
- Heading text: Deep Navy (`#061b31`)
- Body text: Slate (`#64748d`)
- Label text: Dark Slate (`#273951`)
- Border: Soft Blue (`#e5edf5`)
- Link: Stripe Purple (`#533afd`)
- Dark section: Brand Dark (`#1c1e54`)
- Success: Green (`#15be53`)
- Accent decorative: Ruby (`#ea2261`), Magenta (`#f96bee`)

### Example Component Prompts
- "Create a hero section on white background. Headline at 48px sohne-var weight 300, line-height 1.15, letter-spacing -0.96px, color #061b31, font-feature-settings 'ss01'. Subtitle at 18px weight 300, line-height 1.40, color #64748d. Purple CTA button (#533afd, 4px radius, 8px 16px padding, white text) and ghost button (transparent, 1px solid #b9b9f9, #533afd text, 4px radius)."
- "Design a card: white background, 1px solid #e5edf5 border, 6px radius. Shadow: rgba(50,50,93,0.25) 0px 30px 45px -30px, rgba(0,0,0,0.1) 0px 18px 36px -18px. Title at 22px sohne-var weight 300, letter-spacing -0.22px, color #061b31, 'ss01'. Body at 16px weight 300, #64748d."
- "Build a success badge: rgba(21,190,83,0.2) background, #108c3d text, 4px radius, 1px 6px padding, 10px sohne-var weight 300, border 1px solid rgba(21,190,83,0.4)."
- "Create navigation: white sticky header with backdrop-filter blur(12px). sohne-var 14px weight 400 for links, #061b31 text, 'ss01'. Purple CTA 'Start now' right-aligned (#533afd bg, white text, 4px radius). Nav container 6px radius."
- "Design a dark brand section: #1c1e54 background, white text. Headline 32px sohne-var weight 300, letter-spacing -0.64px, 'ss01'. Body 16px weight 300, rgba(255,255,255,0.7). Cards inside use rgba(255,255,255,0.1) border with 6px radius."

### Accessibility Prompt
- "Ensure all interactive elements have a visible focus ring: `outline: 2px solid #533afd; outline-offset: 2px`. Use `:focus-visible` to show the ring only on keyboard navigation. Verify contrast ratios: headings (#061b31 on white) at 15.8:1, body text (#64748d on white) at 4.8:1, purple links (#533afd on white) at 5.2:1. All buttons must meet 44x44px minimum touch targets on mobile. Financial data tables require semantic `<th>` with `scope`, and monetary values need descriptive `aria-label` attributes. Apply `prefers-reduced-motion: reduce` to disable all decorative transitions."

### Iteration Guide
1. Always enable `font-feature-settings: "ss01"` on sohne-var text -- this is the brand's typographic DNA
2. Weight 300 is the default; use 400 only for buttons/links/navigation
3. Shadow formula: `rgba(50,50,93,0.25) 0px Y1 B1 -S1, rgba(0,0,0,0.1) 0px Y2 B2 -S2` where Y1/B1 are larger (far shadow) and Y2/B2 are smaller (near shadow)
4. Heading color is `#061b31` (deep navy), body is `#64748d` (slate), labels are `#273951` (dark slate)
5. Border-radius stays in the 4px-8px range -- never use pill shapes or large rounding
6. Use `"tnum"` for any numbers in tables, charts, or financial displays
7. Dark sections use `#1c1e54` -- not black, not gray, but a deep branded indigo
8. SourceCodePro for code at 12px/500 with 2.00 line-height (very generous for readability)
9. Accessibility is not optional -- focus rings, ARIA labels, contrast ratios, and touch targets are part of the design system, not an afterthought
