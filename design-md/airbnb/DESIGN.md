# Design System Inspiration of Airbnb

## 1. Visual Theme & Atmosphere

Airbnb's website is a warm, photography-forward marketplace that feels like flipping through a travel magazine where every page invites you to book. The design operates on a foundation of pure white (`#ffffff`) with the iconic Rausch Red (`#ff385c`) — named after Airbnb's first street address — serving as the singular brand accent. The result is a clean, airy canvas where listing photography, category icons, and the red CTA button are the only sources of color.

The typography uses Airbnb Cereal VF — a custom variable font that's warm and approachable, with rounded terminals that echo the brand's "belong anywhere" philosophy. The font operates in a tight weight range: 500 (medium) for most UI, 600 (semibold) for emphasis, and 700 (bold) for primary headings. Slight negative letter-spacing (-0.18px to -0.44px) on headings creates a cozy, intimate reading experience rather than the compressed efficiency of tech companies.

What distinguishes Airbnb is its palette-based token system (`--palette-*`) and multi-layered shadow approach. The primary card shadow uses a three-layer stack (`rgba(0,0,0,0.02) 0px 0px 0px 1px, rgba(0,0,0,0.04) 0px 2px 6px, rgba(0,0,0,0.1) 0px 4px 8px`) that creates a subtle, warm lift. Combined with generous border-radius (8px–32px), circular navigation controls (50%), and a category pill bar with horizontal scrolling, the interface feels tactile and inviting — designed for browsing, not commanding.

**Key Characteristics:**
- Pure white canvas with Rausch Red (`#ff385c`) as singular brand accent
- Airbnb Cereal VF — custom variable font with warm, rounded terminals
- Palette-based token system (`--palette-*`) for systematic color management
- Three-layer card shadows: border ring + soft blur + stronger blur
- Generous border-radius: 8px buttons, 14px badges, 20px cards, 32px large elements
- Circular navigation controls (50% radius)
- Photography-first listing cards — images are the hero content
- Near-black text (`#222222`) — warm, not cold
- Luxe Purple (`#460479`) and Plus Magenta (`#92174d`) for premium tiers

## 2. Color Palette & Roles

### Primary Brand
- **Rausch Red** (`#ff385c`): `--palette-bg-primary-core`, primary CTA, brand accent, active states
- **Deep Rausch** (`#e00b41`): `--palette-bg-tertiary-core`, pressed/dark variant of brand red
- **Error Red** (`#c13515`): `--palette-text-primary-error`, error text on light
- **Error Dark** (`#b32505`): `--palette-text-secondary-error-hover`, error hover

### Premium Tiers
- **Luxe Purple** (`#460479`): `--palette-bg-primary-luxe`, Airbnb Luxe tier branding
- **Plus Magenta** (`#92174d`): `--palette-bg-primary-plus`, Airbnb Plus tier branding

### Text Scale
- **Near Black** (`#222222`): `--palette-text-primary`, primary text — warm, not cold
- **Focused Gray** (`#3f3f3f`): `--palette-text-focused`, focused state text
- **Secondary Gray** (`#6a6a6a`): Secondary text, descriptions
- **Disabled** (`rgba(0,0,0,0.24)`): `--palette-text-material-disabled`, disabled state
- **Link Disabled** (`#929292`): `--palette-text-link-disabled`, disabled links

### Interactive
- **Legal Blue** (`#428bff`): `--palette-text-legal`, legal links, informational
- **Border Gray** (`#c1c1c1`): Border color for cards and dividers
- **Light Surface** (`#f2f2f2`): Circular navigation buttons, secondary surfaces

### Surface & Shadows
- **Pure White** (`#ffffff`): Page background, card surfaces
- **Card Shadow** (`rgba(0,0,0,0.02) 0px 0px 0px 1px, rgba(0,0,0,0.04) 0px 2px 6px, rgba(0,0,0,0.1) 0px 4px 8px`): Three-layer warm lift
- **Hover Shadow** (`rgba(0,0,0,0.08) 0px 4px 12px`): Button hover elevation

## 3. Typography Rules

### Font Family
- **Primary**: `Airbnb Cereal VF`, fallbacks: `Circular, -apple-system, system-ui, Roboto, Helvetica Neue`
- **OpenType Features**: `"salt"` (stylistic alternates) on specific caption elements

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|------|--------|-------------|----------------|-------|
| Section Heading | Airbnb Cereal VF | 28px (1.75rem) | 700 | 1.43 | normal | Primary headings |
| Card Heading | Airbnb Cereal VF | 22px (1.38rem) | 600 | 1.18 (tight) | -0.44px | Category/card titles |
| Card Heading Medium | Airbnb Cereal VF | 22px (1.38rem) | 500 | 1.18 (tight) | -0.44px | Lighter variant |
| Sub-heading | Airbnb Cereal VF | 21px (1.31rem) | 700 | 1.43 | normal | Bold sub-headings |
| Feature Title | Airbnb Cereal VF | 20px (1.25rem) | 600 | 1.20 (tight) | -0.18px | Feature headings |
| UI Medium | Airbnb Cereal VF | 16px (1.00rem) | 500 | 1.25 (tight) | normal | Nav, emphasized text |
| UI Semibold | Airbnb Cereal VF | 16px (1.00rem) | 600 | 1.25 (tight) | normal | Strong emphasis |
| Button | Airbnb Cereal VF | 16px (1.00rem) | 500 | 1.25 (tight) | normal | Button labels |
| Body / Link | Airbnb Cereal VF | 14px (0.88rem) | 400 | 1.43 | normal | Standard body |
| Body Medium | Airbnb Cereal VF | 14px (0.88rem) | 500 | 1.29 (tight) | normal | Medium body |
| Caption Salt | Airbnb Cereal VF | 14px (0.88rem) | 600 | 1.43 | normal | `"salt"` feature |
| Small | Airbnb Cereal VF | 13px (0.81rem) | 400 | 1.23 (tight) | normal | Descriptions |
| Tag | Airbnb Cereal VF | 12px (0.75rem) | 400–700 | 1.33 | normal | Tags, prices |
| Badge | Airbnb Cereal VF | 11px (0.69rem) | 600 | 1.18 (tight) | normal | `"salt"` feature |
| Micro Uppercase | Airbnb Cereal VF | 8px (0.50rem) | 700 | 1.25 (tight) | 0.32px | `text-transform: uppercase` |

### Principles
- **Warm weight range**: 500–700 dominate. No weight 300 or 400 for headings — Airbnb's type is always at least medium weight, creating a warm, confident voice.
- **Negative tracking on headings**: -0.18px to -0.44px letter-spacing on display creates intimate, cozy headings rather than cold, compressed ones.
- **"salt" OpenType feature**: Stylistic alternates on specific UI elements (badges, captions) create subtle glyph variations that add visual interest.
- **Variable font precision**: Cereal VF enables continuous weight interpolation, though the design system uses discrete stops at 500, 600, and 700.

### Font Loading Strategy
- **Display strategy**: `font-display: swap` for Airbnb Cereal VF — text renders immediately in the Circular fallback, swapping when the variable font loads
- **Preload**: `<link rel="preload" href="airbnb-cereal-vf.woff2" as="font" type="font/woff2" crossorigin>` for the variable font file — a single file covers the full 500–700 weight range
- **Fallback alignment**: Circular is the primary fallback because it shares similar rounded terminals and warm character with Cereal VF — the swap produces minimal visual disruption. The secondary chain (-apple-system, system-ui, Roboto) provides progressively less similar but universally available alternatives.
- **OpenType preload**: `"salt"` (stylistic alternates) is embedded in the variable font; available immediately after the primary file loads
- **Subset**: Latin subset by default; extended character sets loaded on demand for international market listings

## 4. Component Stylings

### Buttons

**Primary Dark**
- Background: `#222222` (near-black, not pure black)
- Text: `#ffffff`
- Padding: 0px 24px
- Radius: 8px
- Hover: transitions to error/brand accent via `var(--accent-bg-error)`
- Focus: `0 0 0 2px var(--palette-grey1000)` ring + scale(0.92)

**Circular Nav**
- Background: `#f2f2f2`
- Text: `#222222`
- Radius: 50% (circle)
- Hover: shadow `rgba(0,0,0,0.08) 0px 4px 12px` + translateX(50%)
- Active: 4px white border ring + focus shadow
- Focus: scale(0.92) shrink animation

### Cards & Containers
- Background: `#ffffff`
- Radius: 14px (badges), 20px (cards/buttons), 32px (large)
- Shadow: `rgba(0,0,0,0.02) 0px 0px 0px 1px, rgba(0,0,0,0.04) 0px 2px 6px, rgba(0,0,0,0.1) 0px 4px 8px` (three-layer)
- Listing cards: full-width photography on top, details below
- Carousel controls: circular 50% buttons

### Inputs
- Search: `#222222` text
- Focus: `var(--palette-bg-primary-error)` background tint + `0 0 0 2px` ring
- Radius: depends on context (search bar uses pill-like rounding)

### Navigation
- White sticky header with search bar centered
- Airbnb logo (Rausch Red) left-aligned
- Category filter pills: horizontal scroll below search
- Circular nav controls for carousel navigation
- "Become a Host" text link, avatar/menu right-aligned

### Image Treatment
- Listing photography fills card top with generous height
- Image carousel with dot indicators
- Heart/wishlist icon overlay on images
- 8px–14px radius on contained images

## 5. Layout Principles

### Spacing System
- Base unit: 8px
- Scale: 2px, 3px, 4px, 6px, 8px, 10px, 11px, 12px, 15px, 16px, 22px, 24px, 32px

### Grid & Container
- Full-width header with centered search
- Category pill bar: horizontal scrollable row
- Listing grid: responsive multi-column (3–5 columns on desktop)
- Full-width footer with link columns

### Whitespace Philosophy
- **Travel-magazine spacing**: Generous vertical padding between sections creates a leisurely browsing pace — you're meant to scroll slowly, like browsing a magazine.
- **Photography density**: Listing cards are packed relatively tightly, but each image is large enough to feel immersive.
- **Search bar prominence**: The search bar gets maximum vertical space in the header — finding your destination is the primary action.

### Density Modes

Airbnb adapts density based on content context — browsing (discovery) vs. booking (transaction):

| Mode | Vertical Padding | Grid Gap | Use Case |
|------|-----------------|----------|----------|
| Discovery (Default) | 48–80px between sections | 24px grid gap | Search results, listing browsing, category exploration |
| Booking / Transaction | 16–24px between sections | 8–16px | Checkout flow, reservation details, payment forms, host dashboard |

Discovery mode prioritizes visual immersion — large listing photography with generous spacing creates the travel-magazine browsing pace. Booking mode compresses into a transactional density — price breakdowns, date selectors, and guest forms use tight 8–16px spacing. The listing grid itself has its own density: 24px gap between cards on desktop, collapsing to 16px on tablet and 0px (full-bleed cards) on mobile.

**Content-type density rule**: If the user is browsing (looking at listings, exploring categories), use generous discovery spacing. If the user is transacting (booking, paying, managing), use tight transactional spacing. Photography-heavy views always get more breathing room than form-heavy views.

### Border Radius Scale
- Subtle (4px): Small links
- Standard (8px): Buttons, tabs, search elements
- Badge (14px): Status badges, labels
- Card (20px): Feature cards, large buttons
- Large (32px): Large containers, hero elements
- Circle (50%): Nav controls, avatars, icons

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Flat (Level 0) | No shadow | Page background, text blocks |
| Card (Level 1) | `rgba(0,0,0,0.02) 0px 0px 0px 1px, rgba(0,0,0,0.04) 0px 2px 6px, rgba(0,0,0,0.1) 0px 4px 8px` | Listing cards, search bar |
| Hover (Level 2) | `rgba(0,0,0,0.08) 0px 4px 12px` | Button hover, interactive lift |
| Active Focus (Level 3) | `rgb(255,255,255) 0px 0px 0px 4px` + focus ring | Active/focused elements |

**Shadow Philosophy**: Airbnb's three-layer shadow system creates a warm, natural lift. Layer 1 (`0px 0px 0px 1px` at 0.02 opacity) is an ultra-subtle border. Layer 2 (`0px 2px 6px` at 0.04) provides soft ambient shadow. Layer 3 (`0px 4px 8px` at 0.1) adds the primary lift. This graduated approach creates shadows that feel like natural light rather than CSS effects.

## 7. Accessibility

Airbnb is a public accommodation platform — a place where anyone, anywhere should feel welcome. Accessibility is both an ethical imperative and a legal requirement under the ADA. Every listing, every search, every booking flow must work for everyone.

### WCAG Target

**WCAG 2.2 AA** compliance across all user-facing surfaces. Airbnb's mission of belonging anywhere extends to users navigating with screen readers, keyboards, switch devices, and voice control.

### Color Contrast Ratios

| Combination | Ratio | Rating | Notes |
|-------------|-------|--------|-------|
| `#222222` on `#ffffff` | ~15.4:1 | AAA | Primary text — excellent |
| `#6a6a6a` on `#ffffff` | ~5.7:1 | AA | Secondary text — passes |
| `#ff385c` on `#ffffff` | ~3.5:1 | FAILS AA for normal text | Rausch Red must only be used on large text or non-text elements like buttons where the white text on `#222222` carries the readable label |
| `#929292` on `#ffffff` | ~3.0:1 | FAILS | Disabled state — acceptable per WCAG 1.4.3 exception for inactive components |
| `#ffffff` on `#222222` | ~15.4:1 | AAA | White on dark surfaces — excellent |
| `#428bff` on `#ffffff` | ~3.8:1 | Borderline | Legal links should be underlined to not rely solely on color |

### Focus System

All interactive elements receive a visible focus ring: `0 0 0 2px var(--palette-grey1000)` combined with `scale(0.92)`. Focus must be visible on white surfaces and over photography — use a semi-transparent dark backdrop behind the focus ring on image overlays to ensure the ring never disappears against bright listing photos.

### ARIA Patterns

- **Image carousels**: `role="group"`, `aria-roledescription="carousel"`, each slide receives an `aria-label` describing its position and content
- **Heart/wishlist button**: `aria-label="Save to wishlist"`, `aria-pressed` toggled on save
- **Search**: `role="search"` on the search landmark
- **Listing cards**: `role="article"` — each card is a self-contained piece of content
- **Category pill bar**: `role="tablist"` with `role="tab"` on each pill, `aria-selected` on the active category
- **Map pins**: `role="button"`, `aria-label` includes listing name and price (e.g., "Modern loft, 120 dollars per night")
- **Price display**: `aria-label` with full readable text — "150 dollars per night", not "$150"

### Motion Policy

`prefers-reduced-motion` disables:
- `scale(0.92)` focus animation
- `translateX` carousel slide transitions
- Hover shadow transitions on cards and buttons

Image carousels should use instant slide transitions (no slide or fade) when reduced motion is preferred. The experience stays complete — only the movement changes.

### Minimum Touch Targets

Every interactive element meets a 44x44px minimum tap area:
- Circular nav buttons: at least 44px diameter
- Heart overlay on listing images: 44x44px tap area (visual icon can be smaller, tap target cannot)
- Category pills: minimum 44px height with adequate horizontal padding
- Map pins: 44x44px minimum, even when visually compact

### Screen Reader Guidance

- **Listing images**: Descriptive alt text — "Modern apartment with city view in Tokyo", not "listing photo 1"
- **Price breakdowns**: `aria-label` on price containers with the full cost structure
- **Star ratings**: Text equivalent — "4.8 out of 5 stars, 234 reviews", not just the visual stars
- **Map region**: `aria-label` describing the area — "Map showing listings in Shibuya, Tokyo"

## 8. Interaction Patterns

Every tap, hover, and keypress on Airbnb should feel as warm and intentional as the photography. Interactions are gentle — subtle scale shifts, soft shadow lifts, and unhurried transitions that invite exploration rather than demand speed.

### State Machine

**Primary Dark Button (`#222222`)**

| State | Properties |
|-------|------------|
| Default | `background: #222222`, `color: #ffffff`, `border-radius: 8px`, `box-shadow: none` |
| Hover | `background: var(--accent-bg-error)` (brand red transition) |
| Active/Pressed | `transform: scale(0.96)` |
| Focus | `box-shadow: 0 0 0 2px var(--palette-grey1000)`, `transform: scale(0.92)` |
| Disabled | `background: rgba(0,0,0,0.24)`, `cursor: not-allowed` |

**Circular Nav Button**

| State | Properties |
|-------|------------|
| Default | `background: #f2f2f2`, `color: #222222`, `border-radius: 50%` |
| Hover | `box-shadow: rgba(0,0,0,0.08) 0px 4px 12px`, `transform: translateX(50%)` |
| Active/Pressed | `border: 4px solid #ffffff`, focus shadow |
| Focus | `transform: scale(0.92)`, focus ring |
| Disabled | `opacity: 0.5`, `cursor: not-allowed` |

**Listing Card**

| State | Properties |
|-------|------------|
| Default | Three-layer card shadow, `border-radius: 20px` |
| Hover | Enhanced shadow lift, subtle scale or shadow transition |
| Active/Pressed | Slight scale-down feedback |
| Focus | `box-shadow: 0 0 0 2px var(--palette-grey1000)` ring around card |

**Heart/Wishlist Button**

| State | Properties |
|-------|------------|
| Default | Transparent background, white heart with dark shadow outline |
| Hover | Heart fill preview, subtle scale |
| Active/Pressed (saved) | Filled Rausch Red heart, `aria-pressed="true"` |
| Focus | Focus ring visible over image backdrop |

**Search Bar**

| State | Properties |
|-------|------------|
| Default | White background, full card shadow, pill radius |
| Hover | Subtle shadow increase |
| Active/Expanded | Expanded overlay with destination, dates, guests fields |
| Focus | `var(--palette-bg-primary-error)` background tint + `0 0 0 2px` ring |

**Category Pills**

| State | Properties |
|-------|------------|
| Default | `color: #6a6a6a`, no bottom border |
| Hover | `color: #222222`, subtle bottom border preview |
| Active/Selected | `color: #222222`, solid bottom border, `aria-selected="true"` |
| Focus | Focus ring, `transform: scale(0.92)` |

### Transitions

- **Shadows**: `200ms ease` — shadow lifts and drops feel unhurried, like light shifting naturally
- **Scale transforms**: `150ms ease` — snappy enough to feel responsive, soft enough to feel warm
- **Carousel slides**: `300ms ease` — a gentle glide between listing photos
- All transitions respect `prefers-reduced-motion` — when reduced motion is preferred, transitions resolve instantly

### Modals & Overlays

- **Booking modal**: White surface with the three-layer card shadow, focus trap keeps keyboard navigation inside the modal, Escape key closes, `scroll-lock` on the body prevents background scrolling
- **Search expansion overlay**: Expands from the search bar with a smooth animation, dims the background, focus moves into the first search field

### Error States

- **Error text**: `#c13515` (Error Red) — warm but unmistakably alert
- **Error border**: Input border changes to `#c13515` on validation failure
- **Inline messages**: Error description appears directly below the field, 14px Cereal VF weight 400, color `#c13515`
- Form validation is inline and immediate — no jarring page-level error banners

### Loading States

- **Listing card skeleton**: Gray shimmer placeholder at the image aspect ratio (16:10), followed by text-width skeleton bars for title, description, and price
- **Shimmer animation**: Gentle left-to-right gradient sweep, respects `prefers-reduced-motion` (static gray when motion is reduced)
- Skeleton shapes match the final content dimensions to prevent layout shift

### Empty States

- **No results**: Friendly illustration with warm copy — "Try adjusting your search"
- **Adjusted search suggestion**: CTA button offering to expand dates, remove filters, or zoom out on the map
- Empty states never feel like dead ends — there's always a next step

## 9. Responsive Behavior

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile Small | <375px | Single column, compact search |
| Mobile | 375–550px | Standard mobile listing grid |
| Tablet Small | 550–744px | 2-column listings |
| Tablet | 744–950px | Search bar expansion |
| Desktop Small | 950–1128px | 3-column listings |
| Desktop | 1128–1440px | 4-column grid, full header |
| Large Desktop | 1440–1920px | 5-column grid |
| Ultra-wide | >1920px | Maximum grid width |

*Note: Airbnb has 61 detected breakpoints — one of the most granular responsive systems observed, reflecting their obsession with layout at every possible screen size.*

### Fluid Typography

Typography scales fluidly between breakpoints rather than snapping at fixed sizes:
- **Section heading**: `clamp(1.25rem, 3vw, 1.75rem)` — scales from 20px on mobile to 28px on desktop
- **Card heading**: `clamp(1rem, 2.5vw, 1.375rem)` — scales from 16px on mobile to 22px on desktop

### Dark Mode Tokens

Airbnb's warm identity translates into dark mode through carefully chosen surfaces — never pure black, always warm and inviting:

| Token | Light | Dark | Notes |
|-------|-------|------|-------|
| Background | `#ffffff` | `#1a1a1a` | Warm dark, not pure black |
| Text | `#222222` | `#e8e8e8` | Soft white, not harsh `#ffffff` |
| Secondary text | `#6a6a6a` | `#a0a0a0` | Maintains readable contrast |
| Card surface | `#ffffff` | `#262626` | Subtle lift from background |
| Rausch Red | `#ff385c` | `#ff385c` | Brand red stays constant |
| Borders | `rgba(0,0,0,0.02)` | `rgba(255,255,255,0.1)` | Inverted, subtle |
| Shadows | Three-layer at 0.02/0.04/0.1 | `rgba(0,0,0,0.4)` for all three layers | Deeper shadows on dark surfaces |

Warm white surfaces (`#f2f2f2` nav buttons, secondary backgrounds) become `#262626` in dark mode.

**Dark Mode Interactive States**

| State | Property | Light Mode | Dark Mode |
|-------|----------|------------|-----------|
| Primary button hover | Background | `#ff385c` (brand accent) | `#ff5a7a` |
| Circular nav hover | Shadow | `rgba(0,0,0,0.08) 0px 4px 12px` | `rgba(0,0,0,0.3) 0px 4px 12px` |
| Listing card hover | Shadow | Three-layer at 0.02/0.04/0.1 | Three-layer at 0.1/0.15/0.25 |
| Heart button hover | Background | `rgba(0,0,0,0.04)` | `rgba(255,255,255,0.08)` |
| Category pill active | Border-bottom | `2px solid #222222` | `2px solid #e8e8e8` |

### Container Queries

Listing cards adapt their internal layout based on available space rather than viewport width:
- `@container (min-width: 300px)`: Image above text (vertical card layout)
- Below 300px: Side-by-side layout (image left, text right) for compact placements like map sidebars

### Touch Target Sizes

Every interactive element maintains a 44x44px minimum tap area:
- Circular nav buttons: 44px minimum diameter
- Heart overlay: 44x44px tap target
- Category pills: 44px minimum height
- Search bar fields: generously sized for thumb interaction
- Listing cards: full-card tap target on mobile

### Collapsing Strategy
- Listing grid: 5 → 4 → 3 → 2 → 1 columns
- Search: expanded bar → compact bar → overlay
- Category pills: horizontal scroll at all sizes
- Navigation: full header → mobile simplified
- Map: side panel → overlay/toggle

### Image Behavior
- Listing photos: carousel with swipe on mobile
- Responsive image sizing with aspect ratio maintained
- Heart overlay positioned consistently across sizes
- Photo quality adjusts based on viewport

## 10. Do's and Don'ts

### Do
- Use `#222222` (warm near-black) for text — never pure `#000000`
- Apply Rausch Red (`#ff385c`) only for primary CTAs and brand moments — it's the singular accent
- Use Airbnb Cereal VF at weight 500–700 — the warm weight range is intentional
- Apply the three-layer card shadow for all elevated surfaces
- Use generous border-radius: 8px for buttons, 20px for cards, 50% for controls
- Use photography as the primary visual content — listings are image-first
- Apply negative letter-spacing (-0.18px to -0.44px) on headings for intimacy
- Use circular (50%) buttons for carousel/navigation controls

### Don't
- Don't use pure black (`#000000`) for text — always `#222222` (warm)
- Don't apply Rausch Red to backgrounds or large surfaces — it's an accent only
- Don't use thin font weights (300, 400) for headings — 500 minimum
- Don't use heavy shadows (>0.1 opacity as primary layer) — keep them warm and graduated
- Don't use sharp corners (0–4px) on cards — the generous rounding (20px+) is core
- Don't introduce additional brand colors beyond the Rausch/Luxe/Plus system
- Don't override the palette token system — use `--palette-*` variables consistently

## 11. Agent Prompt Guide

### Quick Color Reference
- Background: Pure White (`#ffffff`)
- Text: Near Black (`#222222`)
- Brand accent: Rausch Red (`#ff385c`)
- Secondary text: `#6a6a6a`
- Disabled: `rgba(0,0,0,0.24)`
- Card border: `rgba(0,0,0,0.02) 0px 0px 0px 1px`
- Card shadow: full three-layer stack
- Button surface: `#f2f2f2`

### Example Component Prompts
- "Create a listing card: white background, 20px radius. Three-layer shadow: rgba(0,0,0,0.02) 0px 0px 0px 1px, rgba(0,0,0,0.04) 0px 2px 6px, rgba(0,0,0,0.1) 0px 4px 8px. Photo area on top (16:10 ratio), details below: 16px Airbnb Cereal VF weight 600 title, 14px weight 400 description in #6a6a6a."
- "Design search bar: white background, full card shadow, 32px radius on container. Search text at 14px Cereal VF weight 400. Red search button (#ff385c, 50% radius, white icon)."
- "Build category pill bar: horizontal scrollable row. Each pill: 14px Cereal VF weight 600, #222222 text, bottom border on active. Circular prev/next arrows (#f2f2f2 bg, 50% radius)."
- "Create a CTA button: #222222 background, white text, 8px radius, 16px Cereal VF weight 500, 0px 24px padding. Hover: brand red accent."
- "Design a heart/wishlist button: transparent background, 50% radius, white heart icon with dark shadow outline."

### Accessibility Prompt
Ensure image carousels have `role="group"` and `aria-roledescription="carousel"`. All listing images need descriptive alt text (e.g., "Modern apartment with city view in Tokyo"). Heart/wishlist buttons need `aria-pressed`. Price displays need `aria-label` with full text ("150 dollars per night"). All interactive elements must have 44x44px minimum touch targets.

### Iteration Guide
1. Start with white — the photography provides all the color
2. Rausch Red (#ff385c) is the singular accent — use sparingly for CTAs only
3. Near-black (#222222) for text — the warmth matters
4. Three-layer shadows create natural, warm lift — always use all three layers
5. Generous radius: 8px buttons, 20px cards, 50% controls
6. Cereal VF at 500–700 weight — no thin weights for any heading
7. Photography is hero — every listing card is image-first
