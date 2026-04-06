# Design System Inspiration of Notion

## 1. Visual Theme & Atmosphere

Notion's website embodies the philosophy of the tool itself: a blank canvas that gets out of your way. The design system is built on warm neutrals rather than cold grays, creating a distinctly approachable minimalism that feels like quality paper rather than sterile glass. The page canvas is pure white (`#ffffff`) but the text isn't pure black -- it's a warm near-black (`rgba(0,0,0,0.95)`) that softens the reading experience imperceptibly. The warm gray scale (`#f6f5f4`, `#31302e`, `#615d59`, `#a39e98`) carries subtle yellow-brown undertones, giving the interface a tactile, almost analog warmth.

The custom NotionInter font (a modified Inter) is the backbone of the system. At display sizes (64px), it uses aggressive negative letter-spacing (-2.125px), creating headlines that feel compressed and precise. The weight range is broader than typical systems: 400 for body, 500 for UI elements, 600 for semi-bold labels, and 700 for display headings. OpenType features `"lnum"` (lining numerals) and `"locl"` (localized forms) are enabled on larger text, adding typographic sophistication that rewards close reading.

What makes Notion's visual language distinctive is its border philosophy. Rather than heavy borders or shadows, Notion uses ultra-thin `1px solid rgba(0,0,0,0.1)` borders -- borders that exist as whispers, barely perceptible division lines that create structure without weight. The shadow system is equally restrained: multi-layer stacks with cumulative opacity never exceeding 0.05, creating depth that's felt rather than seen.

**Key Characteristics:**
- NotionInter (modified Inter) with negative letter-spacing at display sizes (-2.125px at 64px)
- Warm neutral palette: grays carry yellow-brown undertones (`#f6f5f4` warm white, `#31302e` warm dark)
- Near-black text via `rgba(0,0,0,0.95)` -- not pure black, creating micro-warmth
- Ultra-thin borders: `1px solid rgba(0,0,0,0.1)` throughout -- whisper-weight division
- Multi-layer shadow stacks with sub-0.05 opacity for barely-there depth
- Notion Blue (`#0075de`) as the singular accent color for CTAs and interactive elements
- Pill badges (9999px radius) with tinted blue backgrounds for status indicators
- 8px base spacing unit with an organic, non-rigid scale

## 2. Color Palette & Roles

### Primary
- **Notion Black** (`rgba(0,0,0,0.95)` / `#000000f2`): Primary text, headings, body copy. The 95% opacity softens pure black without sacrificing readability.
- **Pure White** (`#ffffff`): Page background, card surfaces, button text on blue.
- **Notion Blue** (`#0075de`): Primary CTA, link color, interactive accent -- the only saturated color in the core UI chrome.

### Brand Secondary
- **Deep Navy** (`#213183`): Secondary brand color, used sparingly for emphasis and dark feature sections.
- **Active Blue** (`#005bab`): Button active/pressed state -- darker variant of Notion Blue.

### Warm Neutral Scale
- **Warm White** (`#f6f5f4`): Background surface tint, section alternation, subtle card fill. The yellow undertone is key.
- **Warm Dark** (`#31302e`): Dark surface background, dark section text. Warmer than standard grays.
- **Warm Gray 500** (`#615d59`): Secondary text, descriptions, muted labels.
- **Warm Gray 300** (`#a39e98`): Placeholder text, disabled states, caption text.

### Semantic Accent Colors
- **Teal** (`#2a9d99`): Success states, positive indicators.
- **Green** (`#1aae39`): Confirmation, completion badges.
- **Orange** (`#dd5b00`): Warning states, attention indicators.
- **Pink** (`#ff64c8`): Decorative accent, feature highlights.
- **Purple** (`#391c57`): Premium features, deep accents.
- **Brown** (`#523410`): Earthy accent, warm feature sections.

### Interactive
- **Link Blue** (`#0075de`): Primary link color with underline-on-hover.
- **Link Light Blue** (`#62aef0`): Lighter link variant for dark backgrounds.
- **Focus Blue** (`#097fe8`): Focus ring on interactive elements.
- **Badge Blue Bg** (`#f2f9ff`): Pill badge background, tinted blue surface.
- **Badge Blue Text** (`#097fe8`): Pill badge text, darker blue for readability.

### Shadows & Depth
- **Card Shadow** (`rgba(0,0,0,0.04) 0px 4px 18px, rgba(0,0,0,0.027) 0px 2.025px 7.84688px, rgba(0,0,0,0.02) 0px 0.8px 2.925px, rgba(0,0,0,0.01) 0px 0.175px 1.04062px`): Multi-layer card elevation.
- **Deep Shadow** (`rgba(0,0,0,0.01) 0px 1px 3px, rgba(0,0,0,0.02) 0px 3px 7px, rgba(0,0,0,0.02) 0px 7px 15px, rgba(0,0,0,0.04) 0px 14px 28px, rgba(0,0,0,0.05) 0px 23px 52px`): Five-layer deep elevation for modals and featured content.
- **Whisper Border** (`1px solid rgba(0,0,0,0.1)`): Standard division border -- cards, dividers, sections.

## 3. Typography Rules

### Font Family
- **Primary**: `NotionInter`, with fallbacks: `Inter, -apple-system, system-ui, Segoe UI, Helvetica, Apple Color Emoji, Arial, Segoe UI Emoji, Segoe UI Symbol`
- **OpenType Features**: `"lnum"` (lining numerals) and `"locl"` (localized forms) enabled on display and heading text.

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|------|--------|-------------|----------------|-------|
| Display Hero | NotionInter | 64px (4.00rem) | 700 | 1.00 (tight) | -2.125px | Maximum compression, billboard headlines |
| Display Secondary | NotionInter | 54px (3.38rem) | 700 | 1.04 (tight) | -1.875px | Secondary hero, feature headlines |
| Section Heading | NotionInter | 48px (3.00rem) | 700 | 1.00 (tight) | -1.5px | Feature section titles, with `"lnum"` |
| Sub-heading Large | NotionInter | 40px (2.50rem) | 700 | 1.50 | normal | Card headings, feature sub-sections |
| Sub-heading | NotionInter | 26px (1.63rem) | 700 | 1.23 (tight) | -0.625px | Section sub-titles, content headers |
| Card Title | NotionInter | 22px (1.38rem) | 700 | 1.27 (tight) | -0.25px | Feature cards, list titles |
| Body Large | NotionInter | 20px (1.25rem) | 600 | 1.40 | -0.125px | Introductions, feature descriptions |
| Body | NotionInter | 16px (1.00rem) | 400 | 1.50 | normal | Standard reading text |
| Body Medium | NotionInter | 16px (1.00rem) | 500 | 1.50 | normal | Navigation, emphasized UI text |
| Body Semibold | NotionInter | 16px (1.00rem) | 600 | 1.50 | normal | Strong labels, active states |
| Body Bold | NotionInter | 16px (1.00rem) | 700 | 1.50 | normal | Headlines at body size |
| Nav / Button | NotionInter | 15px (0.94rem) | 600 | 1.33 | normal | Navigation links, button text |
| Caption | NotionInter | 14px (0.88rem) | 500 | 1.43 | normal | Metadata, secondary labels |
| Caption Light | NotionInter | 14px (0.88rem) | 400 | 1.43 | normal | Body captions, descriptions |
| Badge | NotionInter | 12px (0.75rem) | 600 | 1.33 | 0.125px | Pill badges, tags, status labels |
| Micro Label | NotionInter | 12px (0.75rem) | 400 | 1.33 | 0.125px | Small metadata, timestamps |

### Principles
- **Compression at scale**: NotionInter at display sizes uses -2.125px letter-spacing at 64px, progressively relaxing to -0.625px at 26px and normal at 16px. The compression creates density at headlines while maintaining readability at body sizes.
- **Four-weight system**: 400 (body/reading), 500 (UI/interactive), 600 (emphasis/navigation), 700 (headings/display). The broader weight range compared to most systems allows nuanced hierarchy.
- **Warm scaling**: Line height tightens as size increases -- 1.50 at body (16px), 1.23-1.27 at sub-headings, 1.00-1.04 at display. This creates denser, more impactful headlines.
- **Badge micro-tracking**: The 12px badge text uses positive letter-spacing (0.125px) -- the only positive tracking in the system, creating wider, more legible small text.

### Font Loading Strategy
- **Display strategy**: `font-display: swap` for NotionInter — text renders immediately in the Inter fallback (nearly identical metrics), swapping when the custom variant loads
- **Preload**: `<link rel="preload" href="notioninter.woff2" as="font" type="font/woff2" crossorigin>` for weight 400 (most common). Weights 500, 600, 700 load on demand.
- **Fallback alignment**: Inter is the primary fallback because NotionInter is a modified Inter — the metrics are nearly identical, producing minimal layout shift on swap. This is one of the best fallback chains in modern web design.
- **OpenType preload**: `"lnum"` and `"locl"` features are embedded in the font file; no additional request needed once the primary file loads
- **Subset**: Latin subset by default; CJK and extended ranges loaded asynchronously for internationalized workspaces

## 4. Component Stylings

### Buttons

**Primary Blue**
- Background: `#0075de` (Notion Blue)
- Text: `#ffffff`
- Padding: 8px 16px
- Radius: 4px (subtle)
- Border: `1px solid transparent`
- Hover: background darkens to `#005bab`
- Active: scale(0.9) transform
- Focus: `2px solid` focus outline, `var(--shadow-level-200)` shadow
- Use: Primary CTA ("Get Notion free", "Try it")

**Secondary / Tertiary**
- Background: `rgba(0,0,0,0.05)` (translucent warm gray)
- Text: `#000000` (near-black)
- Padding: 8px 16px
- Radius: 4px
- Hover: text color shifts, scale(1.05)
- Active: scale(0.9) transform
- Use: Secondary actions, form submissions

**Ghost / Link Button**
- Background: transparent
- Text: `rgba(0,0,0,0.95)`
- Decoration: underline on hover
- Use: Tertiary actions, inline links

**Pill Badge Button**
- Background: `#f2f9ff` (tinted blue)
- Text: `#097fe8`
- Padding: 4px 8px
- Radius: 9999px (full pill)
- Font: 12px weight 600
- Use: Status badges, feature labels, "New" tags

### Cards & Containers
- Background: `#ffffff`
- Border: `1px solid rgba(0,0,0,0.1)` (whisper border)
- Radius: 12px (standard cards), 16px (featured/hero cards)
- Shadow: `rgba(0,0,0,0.04) 0px 4px 18px, rgba(0,0,0,0.027) 0px 2.025px 7.84688px, rgba(0,0,0,0.02) 0px 0.8px 2.925px, rgba(0,0,0,0.01) 0px 0.175px 1.04062px`
- Hover: subtle shadow intensification
- Image cards: 12px top radius, image fills top half

### Inputs & Forms
- Background: `#ffffff`
- Text: `rgba(0,0,0,0.9)`
- Border: `1px solid #dddddd`
- Padding: 6px
- Radius: 4px
- Focus: blue outline ring
- Placeholder: warm gray `#a39e98`

### Navigation
- Clean horizontal nav on white, not sticky
- Brand logo left-aligned (33x34px icon + wordmark)
- Links: NotionInter 15px weight 500-600, near-black text
- Hover: color shift to `var(--color-link-primary-text-hover)`
- CTA: blue pill button ("Get Notion free") right-aligned
- Mobile: hamburger menu collapse
- Product dropdowns with multi-level categorized menus

### Image Treatment
- Product screenshots with `1px solid rgba(0,0,0,0.1)` border
- Top-rounded images: `12px 12px 0px 0px` radius
- Dashboard/workspace preview screenshots dominate feature sections
- Warm gradient backgrounds behind hero illustrations (decorative character illustrations)

### Distinctive Components

**Feature Cards with Illustrations**
- Large illustrative headers (The Great Wave, product UI screenshots)
- 12px radius card with whisper border
- Title at 22px weight 700, description at 16px weight 400
- Warm white (`#f6f5f4`) background variant for alternating sections

**Trust Bar / Logo Grid**
- Company logos (trusted teams section) in their brand colors
- Horizontal scroll or grid layout with team counts
- Metric display: large number + description pattern

**Metric Cards**
- Large number display (e.g., "$4,200 ROI")
- NotionInter 40px+ weight 700 for the metric
- Description below in warm gray body text
- Whisper-bordered card container

## 5. Layout Principles

### Spacing System
- Base unit: 8px
- Scale: 2px, 3px, 4px, 5px, 6px, 7px, 8px, 11px, 12px, 14px, 16px, 24px, 32px
- Non-rigid organic scale with fractional values (5.6px, 6.4px) for micro-adjustments
- **Interpolation rule**: Notion's scale is intentionally organic — fractional values are acceptable for optical alignment, but only when derived from the base unit (e.g., 6.4px = 0.8 * 8px). For component spacing use the defined integer values; reserve fractional values for sub-pixel adjustments in icon and text alignment only.

### Grid & Container
- Max content width: approximately 1200px
- Hero: centered single-column with generous top padding (80-120px)
- Feature sections: 2-3 column grids for cards
- Full-width warm white (`#f6f5f4`) section backgrounds for alternation
- Code/dashboard screenshots as contained with whisper border

### Whitespace Philosophy
- **Generous vertical rhythm**: 64-120px between major sections. Notion lets content breathe with vast vertical padding.
- **Warm alternation**: White sections alternate with warm white (`#f6f5f4`) sections, creating gentle visual rhythm without harsh color breaks.
- **Content-first density**: Body text blocks are compact (line-height 1.50) but surrounded by ample margin, creating islands of readable content in a sea of white space.

### Density Modes

Notion's design adapts density based on whether the user is browsing the marketing site or using the product workspace:

| Mode | Vertical Padding | Grid Gap | Use Case |
|------|-----------------|----------|----------|
| Marketing (Default) | 64–120px between sections | 24–32px | Landing pages, feature showcases, pricing |
| Workspace / Product | 4–12px between blocks | 0–8px | Document editor, database views, sidebar navigation |

The marketing site uses the generous vertical rhythm described above. Notion's workspace operates at extreme density — document blocks have 4px vertical margins, database rows use 8px padding, sidebar items use 4px gaps. The warm white (#f6f5f4) section alternation applies only to marketing; the workspace is consistently white or warm white without alternation.

**Content-type density rule**: Marketing pages use generous breathing room to showcase features. Product/workspace interfaces use tight density because users are creating and organizing — every pixel of screen real estate matters. The 8px base unit applies at both densities.

### Border Radius Scale
- Micro (4px): Buttons, inputs, functional interactive elements
- Subtle (5px): Links, list items, menu items
- Standard (8px): Small cards, containers, inline elements
- Comfortable (12px): Standard cards, feature containers, image tops
- Large (16px): Hero cards, featured content, promotional blocks
- Full Pill (9999px): Badges, pills, status indicators
- Circle (100%): Tab indicators, avatars

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Flat (Level 0) | No shadow, no border | Page background, text blocks |
| Whisper (Level 1) | `1px solid rgba(0,0,0,0.1)` | Standard borders, card outlines, dividers |
| Soft Card (Level 2) | 4-layer shadow stack (max opacity 0.04) | Content cards, feature blocks |
| Deep Card (Level 3) | 5-layer shadow stack (max opacity 0.05, 52px blur) | Modals, featured panels, hero elements |
| Focus (Accessibility) | `2px solid var(--focus-color)` outline | Keyboard focus on all interactive elements |

**Shadow Philosophy**: Notion's shadow system uses multiple layers with extremely low individual opacity (0.01 to 0.05) that accumulate into soft, natural-looking elevation. The 4-layer card shadow spans from 1.04px to 18px blur, creating a gradient of depth rather than a single hard shadow. The 5-layer deep shadow extends to 52px blur at 0.05 opacity, producing ambient occlusion that feels like natural light rather than computer-generated depth. This layered approach makes elements feel embedded in the page rather than floating above it.

### Decorative Depth
- Hero section: decorative character illustrations (playful, hand-drawn style)
- Section alternation: white to warm white (`#f6f5f4`) background shifts
- No hard section borders -- separation comes from background color changes and spacing

## 7. Accessibility

Notion's design system treats accessibility as a natural extension of its warm, approachable philosophy. The same restraint that produces whisper borders and soft shadows also produces clear, readable interfaces that work for everyone. The target is **WCAG 2.2 AA** compliance across all interactive surfaces.

### Color Contrast

| Pairing | Ratio | Rating | Notes |
|---------|-------|--------|-------|
| `rgba(0,0,0,0.95)` on `#ffffff` | ~18:1 | AAA | Primary text -- exceeds all thresholds comfortably |
| `#615d59` on `#ffffff` | ~5.5:1 | AA | Secondary text -- passes AA for all sizes |
| `#a39e98` on `#ffffff` | ~2.6:1 | Fails AA | Warm Gray 300 -- suitable only for decorative or non-essential text. Do not use for meaningful labels or body copy. |
| `#0075de` on `#ffffff` | ~4.6:1 | AA large text | Notion Blue CTA -- passes AA for large text (18px+ or 14px bold). CTA buttons at 15px weight 600 may be borderline; pair with sufficient button sizing. |
| `#097fe8` on `#f2f9ff` | ~4.5:1 | AA large text | Badge text on badge background -- acceptable at badge scale given pill context, but borderline for smaller sizes. |

### Focus System
- All interactive elements receive visible focus indicators
- Focus outline: `2px solid` with focus color (`#097fe8`) + shadow level 200 for reinforcement
- Focus indicators must remain visible on both white (`#ffffff`) and warm white (`#f6f5f4`) backgrounds -- the blue outline + shadow combination ensures this
- Tab navigation supported throughout all interactive components
- Focus order follows visual reading order: left-to-right, top-to-bottom

### ARIA Patterns
- **Buttons**: Native `<button>` elements preferred. Icon-only buttons require `aria-label` describing the action.
- **Navigation**: Product dropdowns use `aria-expanded` on trigger and `aria-haspopup="true"`. Mobile hamburger menu uses `aria-expanded` and `aria-controls`.
- **Cards**: Use `<article>` with `aria-labelledby` pointing to the card title. Linked cards wrap the title in the anchor, not the entire card surface.
- **Workspace Screenshots**: Product screenshots that convey information use `role="img"` with a descriptive `aria-label` summarizing what the screenshot shows.
- **Feature Illustrations**: Decorative hero illustrations and character art use `alt=""` and `aria-hidden="true"` -- they add warmth, not information.

### Motion Policy
- `prefers-reduced-motion: reduce` disables the `scale(0.9)` active transform and `scale(1.05)` hover transform on buttons
- Shadow transitions (hover intensification) are also disabled under reduced motion
- Page scroll remains unaffected -- reduced motion targets animated transforms and transitions only
- Implementation: wrap motion-dependent transitions in `@media (prefers-reduced-motion: no-preference) { ... }`

### Touch Target Sizes
- Mobile: minimum 44x44px touch target on all interactive elements (following WCAG 2.5.8)
- Desktop: minimum 36px height on clickable elements (buttons, links, nav items)
- Pill badges used as interactive elements must meet touch target minimums through padding expansion, not visual size increase

### Screen Reader Guidance
- Heading hierarchy is semantic: a single `<h1>` per page, `<h2>` for major sections, `<h3>` for subsections. The visual hierarchy (64px display, 48px section, 26px sub-heading) maps directly to heading levels.
- The warm white section alternation (white to `#f6f5f4`) must not be the only structural cue. Each section needs a heading or landmark role so screen reader users perceive the same rhythm sighted users feel through the background color shifts.
- Long feature card grids use list markup (`<ul>` / `<li>`) so screen readers announce item count and position.

## 8. Interaction Patterns

Notion's interactions follow the same philosophy as its visual design: restrained, warm, and felt rather than flashy. Every state change is subtle -- a gentle shift rather than a dramatic transformation.

### State Machine

| State | Buttons | Cards | Links | Inputs | Badges |
|-------|---------|-------|-------|--------|--------|
| **Default** | Solid fill, whisper border | White bg, whisper border, soft shadow | Near-black text, no underline | White bg, `#dddddd` border | `#f2f9ff` bg, `#097fe8` text |
| **Hover** | Color shift (blue darkens to `#005bab`), scale(1.05) | Shadow intensification, subtle lift | Color shift, underline appears | Border darkens | Slight background darken |
| **Active** | scale(0.9), darker bg (`#005bab`) | scale(0.98) press effect | Darker color | -- | -- |
| **Focus** | `2px solid #097fe8` outline + shadow level 200 | `2px solid #097fe8` outline | `2px solid #097fe8` outline | Blue outline ring, shadow | `2px solid #097fe8` outline |
| **Disabled** | Warm gray `#a39e98` text, reduced opacity (0.5), no pointer events | Muted shadow, reduced contrast | Warm gray text, no underline | `#f6f5f4` bg, `#a39e98` text | Reduced opacity |

### Transitions
- **Color changes**: `150ms ease` -- fast enough to feel instant, slow enough to feel intentional
- **Transform and shadow**: `200ms ease` -- slightly longer for spatial changes so the movement reads clearly
- **All transitions** respect `prefers-reduced-motion`: under reduced motion, state changes are instant (0ms duration) while color shifts remain

### Modals & Overlays
- Focus trap: keyboard focus cycles within the modal while open, never escaping to background content
- `Escape` key closes the modal and returns focus to the trigger element
- Scroll lock: page scroll is disabled while modal is open (`overflow: hidden` on body)
- Backdrop: `rgba(0,0,0,0.5)` overlay, clicking outside the modal dismisses it
- Entry/exit: gentle opacity fade, no dramatic scale transforms

### Error States
- Inline validation messages appear directly below the input field
- Border color shifts from `#dddddd` to a warm red on invalid fields
- Error text uses 14px weight 500 in a readable red -- never relies on color alone (an error icon accompanies the message)
- Errors appear on blur or submit, not on every keystroke

### Loading States
- Skeleton screens use warm white (`#f6f5f4`) as the base with a subtle shimmer animation
- Skeleton shapes mirror the content they replace: rounded rectangles for text lines, 12px radius blocks for cards
- Shimmer uses a left-to-right gradient sweep at `1.5s` duration
- Under `prefers-reduced-motion`, the shimmer is replaced with a static warm white block

### Empty States
- A warm, hand-drawn style illustration centered above the message (consistent with Notion's decorative character illustrations)
- Muted text in warm gray (`#615d59`) at 16px weight 400 explaining what belongs here
- A single Notion Blue CTA button inviting the user to take the first action
- No heavy borders or shadows -- the empty state is quiet and inviting, not alarming

## 9. Responsive Behavior

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile Small | <400px | Tight single column, minimal padding |
| Mobile | 400-600px | Standard mobile, stacked layout |
| Tablet Small | 600-768px | 2-column grids begin |
| Tablet | 768-1080px | Full card grids, expanded padding |
| Desktop Small | 1080-1200px | Standard desktop layout |
| Desktop | 1200-1440px | Full layout, maximum content width |
| Large Desktop | >1440px | Centered, generous margins |

### Fluid Typography
- **Display**: `clamp(2rem, 5vw, 4rem)` -- scales fluidly from 32px on mobile to 64px on desktop, maintaining the compressed letter-spacing proportionally
- **Section heading**: `clamp(1.5rem, 4vw, 3rem)` -- 24px to 48px, keeping the tight line-height throughout
- Letter-spacing scales proportionally with font size: the compression ratio stays consistent even as the rendered size changes

### Touch Target Sizes
- Buttons: minimum 44px height on mobile (8px vertical padding expands to 12px), 36px desktop minimum
- Navigation links: 44px tap target height on mobile via padding, 15px font with 14px vertical padding
- Pill badges: 32px minimum height when interactive, expanded via vertical padding
- Mobile menu toggle: 44x44px minimum
- Card tap targets: entire card surface is tappable on mobile, minimum 48px vertical content area

### Dark Mode Tokens
| Token | Light | Dark | Notes |
|-------|-------|------|-------|
| Background | `#ffffff` | `#191919` | Warm dark, not pure black |
| Text primary | `rgba(0,0,0,0.95)` | `rgba(255,255,255,0.9)` | Softened white, matching the light mode philosophy |
| Text secondary | `#615d59` | `#888888` | Lifted gray for readability on dark surfaces |
| Warm surface | `#f6f5f4` | `#252525` | Section alternation continues in dark mode |
| Borders | `rgba(0,0,0,0.1)` | `rgba(255,255,255,0.1)` | Same whisper weight, inverted |
| Notion Blue | `#0075de` | `#0075de` | Blue stays constant across modes |
| Card shadow opacity | 0.04 max | 0.08-0.1 max | Increased opacity for visibility against dark backgrounds |

**Dark Mode Interactive States**

| State | Property | Light Mode | Dark Mode |
|-------|----------|------------|-----------|
| Primary button hover | Background | `#005bab` | `#3399ff` |
| Secondary button hover | Background | `rgba(0,0,0,0.08)` | `rgba(255,255,255,0.08)` |
| Card hover | Shadow opacity | 0.04 max layer | 0.10 max layer |
| Link hover | Color | `#005bab` | `#66b3ff` |
| Input focus | Border | `1px solid #0075de` | `1px solid #3399ff` |

### Container Queries
- Feature cards adapt layout at `@container (min-width: 400px)` -- below this threshold, card content stacks vertically; above, illustration and text sit side-by-side
- Container queries are preferred over media queries for component-level layout decisions, keeping cards responsive regardless of their placement context

### Collapsing Strategy
- Hero: 64px display -> scales fluidly via clamp -> 26px floor on mobile, maintains proportional letter-spacing
- Navigation: horizontal links + blue CTA -> hamburger menu
- Feature cards: 3-column -> 2-column -> single column stacked
- Product screenshots: maintain aspect ratio with responsive images
- Trust bar logos: grid -> horizontal scroll on mobile
- Footer: multi-column -> stacked single column
- Section spacing: 80px+ -> 48px on mobile

### Image Behavior
- Workspace screenshots maintain whisper border at all sizes
- Hero illustrations scale proportionally
- Product screenshots use responsive images with consistent border radius
- Full-width warm white sections maintain edge-to-edge treatment

## 10. Do's and Don'ts

### Do
- Use warm neutrals with yellow-brown undertones (`#f6f5f4`, `#31302e`, `#615d59`) -- never blue-gray
- Use `rgba(0,0,0,0.95)` for text, not pure `#000000`
- Apply whisper borders: `1px solid rgba(0,0,0,0.1)`
- Use NotionInter with negative letter-spacing at display sizes
- Enable `"lnum"` and `"locl"` OpenType features on headings
- Use four weights: 400 (body), 500 (UI), 600 (emphasis), 700 (display)
- Alternate white and warm white (`#f6f5f4`) sections for rhythm
- Use Notion Blue (`#0075de`) as the singular accent color

### Don't
- Don't use cold grays or blue-tinted neutrals
- Don't use heavy borders -- `1px` at `rgba(0,0,0,0.1)` maximum
- Don't use shadows with individual layer opacity above 0.05
- Don't use pill radius (`9999px`) on action buttons -- pills are for badges only
- Don't introduce additional saturated colors beyond Notion Blue for core UI
- Don't skip the warm white section alternation -- it's the visual rhythm
- Don't use positive letter-spacing except on 12px badge text

## 11. Agent Prompt Guide

### Quick Color Reference
- Primary CTA: Notion Blue (`#0075de`)
- Background: Pure White (`#ffffff`)
- Alt Background: Warm White (`#f6f5f4`)
- Heading text: Near-Black (`rgba(0,0,0,0.95)`)
- Body text: Near-Black (`rgba(0,0,0,0.95)`)
- Secondary text: Warm Gray 500 (`#615d59`)
- Muted text: Warm Gray 300 (`#a39e98`)
- Border: `1px solid rgba(0,0,0,0.1)`
- Link: Notion Blue (`#0075de`)
- Focus ring: Focus Blue (`#097fe8`)

### Example Component Prompts
- "Create a hero section on white background. Headline at 64px NotionInter weight 700, line-height 1.00, letter-spacing -2.125px, color rgba(0,0,0,0.95). Subtitle at 20px weight 600, line-height 1.40, color #615d59. Blue CTA button (#0075de, 4px radius, 8px 16px padding, white text) and ghost button (transparent bg, near-black text, underline on hover)."
- "Design a card: white background, 1px solid rgba(0,0,0,0.1) border, 12px radius. Use shadow stack: rgba(0,0,0,0.04) 0px 4px 18px, rgba(0,0,0,0.027) 0px 2.025px 7.85px, rgba(0,0,0,0.02) 0px 0.8px 2.93px, rgba(0,0,0,0.01) 0px 0.175px 1.04px. Title at 22px NotionInter weight 700, letter-spacing -0.25px. Body at 16px weight 400, color #615d59."
- "Build a pill badge: #f2f9ff background, #097fe8 text, 9999px radius, 4px 8px padding, 12px NotionInter weight 600, letter-spacing 0.125px."
- "Create navigation: white header. NotionInter 15px weight 600 for links, near-black text. Blue pill CTA 'Get Notion free' right-aligned (#0075de bg, white text, 4px radius)."
- "Design an alternating section layout: white sections alternate with warm white (#f6f5f4) sections. Each section has 64-80px vertical padding, max-width 1200px centered. Section heading at 48px weight 700, line-height 1.00, letter-spacing -1.5px."

### Accessibility Prompt
- "Ensure all interactive elements have visible focus indicators: 2px solid #097fe8 outline with shadow reinforcement. Touch targets are 44x44px minimum on mobile, 36px height minimum on desktop. Use semantic heading hierarchy (h1 > h2 > h3) mapping to visual sizes. Decorative illustrations get alt=''. Product screenshots get descriptive aria-label. Respect prefers-reduced-motion by disabling scale transforms and shadow transitions. Verify color contrast: primary text at ~18:1, secondary at ~5.5:1, avoid #a39e98 for essential content (~2.6:1 fails AA)."

### Iteration Guide
1. Always use warm neutrals -- Notion's grays have yellow-brown undertones (#f6f5f4, #31302e, #615d59, #a39e98), never blue-gray
2. Letter-spacing scales with font size: -2.125px at 64px, -1.875px at 54px, -0.625px at 26px, normal at 16px
3. Four weights: 400 (read), 500 (interact), 600 (emphasize), 700 (announce)
4. Borders are whispers: 1px solid rgba(0,0,0,0.1) -- never heavier
5. Shadows use 4-5 layers with individual opacity never exceeding 0.05
6. The warm white (#f6f5f4) section background is essential for visual rhythm
7. Pill badges (9999px) for status/tags, 4px radius for buttons and inputs
8. Notion Blue (#0075de) is the only saturated color in core UI -- use it sparingly for CTAs and links
