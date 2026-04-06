<a href="https://github.com/VoltAgent/voltagent">
     <img alt="Awesome DESIGN.md — curated design system files for AI agents" src="https://github.com/user-attachments/assets/d012a0d2-cec3-4630-ba5e-acc339dbe6cf" />
</a>

<br/>
<br/>

<div align="center">
    <strong>Ready-to-use DESIGN.md files extracted from 58 developer-focused websites.</strong>
    <br />
    <br />

</div>

<div align="center">

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
![DESIGN.md Count](https://img.shields.io/badge/DESIGN.md%20count-58-10b981?style=classic)
[![Last Update](https://img.shields.io/github/last-commit/VoltAgent/awesome-design-md?label=Last%20update&style=classic)](https://github.com/VoltAgent/awesome-design-md)
[![Discord](https://img.shields.io/discord/1361559153780195478.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://s.voltagent.dev/discord)

</div>

# Awesome DESIGN.md

Copy a DESIGN.md into your project, tell your AI agent "build me a page that looks like this" and get pixel-perfect UI that actually matches.

## Table of Contents

- [What is DESIGN.md?](#what-is-designmd)
- [What's Inside Each DESIGN.md](#whats-inside-each-designmd)
- [How to Use](#how-to-use)
- [Collection](#collection) — [AI & ML](#ai--machine-learning-12) | [Dev Tools](#developer-tools--platforms-14) | [Infrastructure](#infrastructure--cloud-6) | [Design](#design--productivity-10) | [Fintech](#fintech--crypto-4) | [Enterprise](#enterprise--consumer-7) | [Automotive](#automotive-5)
- [Request a DESIGN.md](#request-a-designmd)
- [Contributing](#contributing)


## What is DESIGN.md?

[DESIGN.md](https://stitch.withgoogle.com/docs/design-md/overview/) is a concept introduced by Google Stitch. A plain-text design system document that AI agents read to generate consistent UI.

It's a markdown file. No Figma exports, no JSON schemas, no special tooling. Drop it into your project root and any AI coding agent or Google Stitch instantly understands how your UI should look. Markdown is the format LLMs read best, so there's nothing to parse or configure.

| File | Who reads it | What it defines |
|------|-------------|-----------------|
| `AGENTS.md` | Coding agents | How to build the project |
| `DESIGN.md` | Design agents | How the project should look, feel, and behave |

**This repo provides ready-to-use DESIGN.md files** extracted from real websites.



## What's Inside Each DESIGN.md

Every file follows the [Stitch DESIGN.md format](https://stitch.withgoogle.com/docs/design-md/format/) with extended sections:

| # | Section | What it captures |
|---|---------|-----------------|
| 1 | Visual Theme & Atmosphere | Mood, density, design philosophy |
| 2 | Color Palette & Roles | Semantic name + hex + functional role |
| 3 | Typography Rules | Font families, full hierarchy table, fluid type scale |
| 4 | Component Stylings | Buttons, cards, inputs, navigation with states |
| 5 | Layout Principles | Spacing scale, grid, density modes, whitespace philosophy |
| 6 | Depth & Elevation | Shadow system, surface hierarchy |
| 7 | Accessibility | WCAG target, contrast ratios, focus system, ARIA patterns, motion policy, minimum touch targets |
| 8 | Interaction Patterns | State machine (default/hover/active/focus/disabled), transitions, motion, modals, error states |
| 9 | Responsive Behavior | Breakpoints, fluid typography, container queries, touch targets, dark mode tokens, collapsing strategy |
| 10 | Do's and Don'ts | Design guardrails and anti-patterns |
| 11 | Agent Prompt Guide | Quick color reference, ready-to-use prompts |

Each site includes:

| File | Purpose |
|------|---------|
| `DESIGN.md` | The design system (what agents read) |
| `preview.html` | Visual catalog showing color swatches, type scale, buttons, cards |
| `preview-dark.html` | Same catalog with dark surfaces |

### How to Use

1. **Pick a DESIGN.md** from the [collection](#collection) that matches the visual style you want
2. **Copy it** into your project root (or a `docs/` folder)
3. **Tell your AI agent** to use it — e.g., "build me a landing page following DESIGN.md"

Works with Claude Code, Cursor, GitHub Copilot, Google Stitch, and any agent that reads project context files. The DESIGN.md format is agent-agnostic — it's plain markdown that any LLM can interpret.


## Request a DESIGN.md

[Open a GitHub issue with this template](https://github.com/VoltAgent/awesome-design-md/issues/new?template=design-md-request.yml) to request a DESIGN.md generation for a website.

---

## Collection

### AI & Machine Learning (12)

- [**Claude**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/claude/) — Anthropic's AI assistant. Warm terracotta accent, clean editorial layout
- [**Cohere**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/cohere/) — Enterprise AI platform. Vibrant gradients, data-rich dashboard aesthetic
- [**ElevenLabs**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/elevenlabs/) — AI voice platform. Dark cinematic UI, audio-waveform aesthetics
- [**Minimax**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/minimax/) — AI model provider. Bold dark interface with neon accents
- [**Mistral AI**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/mistral.ai/) — Open-weight LLM provider. French-engineered minimalism, purple-toned
- [**Ollama**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/ollama/) — Run LLMs locally. Terminal-first, monochrome simplicity
- [**OpenCode AI**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/opencode.ai/) — AI coding platform. Developer-centric dark theme
- [**Replicate**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/replicate/) — Run ML models via API. Clean white canvas, code-forward
- [**RunwayML**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/runwayml/) — AI video generation. Cinematic dark UI, media-rich layout
- [**Together AI**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/together.ai/) — Open-source AI infrastructure. Technical, blueprint-style design
- [**VoltAgent**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/voltagent/) — AI agent framework. Void-black canvas, emerald accent, terminal-native
- [**xAI**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/x.ai/) — Elon Musk's AI lab. Stark monochrome, futuristic minimalism

---

### Developer Tools & Platforms (14)

- [**Cursor**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/cursor/) — AI-first code editor. Sleek dark interface, gradient accents
- [**Expo**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/expo/) — React Native platform. Dark theme, tight letter-spacing, code-centric
- [**Linear**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/linear.app/) — Project management for engineers. Ultra-minimal, precise, purple accent
- [**Lovable**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/lovable/) — AI full-stack builder. Playful gradients, friendly dev aesthetic
- [**Mintlify**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/mintlify/) — Documentation platform. Clean, green-accented, reading-optimized
- [**PostHog**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/posthog/) — Product analytics. Playful hedgehog branding, developer-friendly dark UI
- [**Raycast**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/raycast/) — Productivity launcher. Sleek dark chrome, vibrant gradient accents
- [**Resend**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/resend/) — Email API for developers. Minimal dark theme, monospace accents
- [**Sentry**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/sentry/) — Error monitoring. Dark dashboard, data-dense, pink-purple accent
- [**Supabase**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/supabase/) — Open-source Firebase alternative. Dark emerald theme, code-first
- [**Superhuman**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/superhuman/) — Fast email client. Premium dark UI, keyboard-first, purple glow
- [**Vercel**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/vercel/) — Frontend deployment platform. Black and white precision, Geist font
- [**Warp**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/warp/) — Modern terminal. Dark IDE-like interface, block-based command UI
- [**Zapier**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/zapier/) — Automation platform. Warm orange, friendly illustration-driven

---

### Infrastructure & Cloud (6)

- [**ClickHouse**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/clickhouse/) — Fast analytics database. Yellow-accented, technical documentation style
- [**Composio**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/composio/) — Tool integration platform. Modern dark with colorful integration icons
- [**HashiCorp**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/hashicorp/) — Infrastructure automation. Enterprise-clean, black and white
- [**MongoDB**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/mongodb/) — Document database. Green leaf branding, developer documentation focus
- [**Sanity**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/sanity/) — Headless CMS. Red accent, content-first editorial layout
- [**Stripe**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/stripe/) — Payment infrastructure. Signature purple gradients, weight-300 elegance

---

### Design & Productivity (10)

- [**Airtable**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/airtable/) — Spreadsheet-database hybrid. Colorful, friendly, structured data aesthetic
- [**Cal.com**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/cal/) — Open-source scheduling. Clean neutral UI, developer-oriented simplicity
- [**Clay**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/clay/) — Creative agency. Organic shapes, soft gradients, art-directed layout
- [**Figma**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/figma/) — Collaborative design tool. Vibrant multi-color, playful yet professional
- [**Framer**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/framer/) — Website builder. Bold black and blue, motion-first, design-forward
- [**Intercom**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/intercom/) — Customer messaging. Friendly blue palette, conversational UI patterns
- [**Miro**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/miro/) — Visual collaboration. Bright yellow accent, infinite canvas aesthetic
- [**Notion**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/notion/) — All-in-one workspace. Warm minimalism, serif headings, soft surfaces
- [**Pinterest**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/pinterest/) — Visual discovery platform. Red accent, masonry grid, image-first
- [**Webflow**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/webflow/) — Visual web builder. Blue-accented, polished marketing site aesthetic

---

### Fintech & Crypto (4)

- [**Coinbase**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/coinbase/) — Crypto exchange. Clean blue identity, trust-focused, institutional feel
- [**Kraken**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/kraken/) — Crypto trading platform. Purple-accented dark UI, data-dense dashboards
- [**Revolut**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/revolut/) — Digital banking. Sleek dark interface, gradient cards, fintech precision
- [**Wise**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/wise/) — International money transfer. Bright green accent, friendly and clear

---

### Enterprise & Consumer (7)

- [**Airbnb**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/airbnb/) — Travel marketplace. Warm coral accent, photography-driven, rounded UI
- [**Apple**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/apple/) — Consumer electronics. Premium white space, SF Pro, cinematic imagery
- [**IBM**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/ibm/) — Enterprise technology. Carbon design system, structured blue palette
- [**NVIDIA**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/nvidia/) — GPU computing. Green-black energy, technical power aesthetic
- [**SpaceX**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/spacex/) — Space technology. Stark black and white, full-bleed imagery, futuristic
- [**Spotify**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/spotify/) — Music streaming. Vibrant green on dark, bold type, album-art-driven
- [**Uber**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/uber/) — Mobility platform. Bold black and white, tight type, urban energy

---

### Automotive (5)

- [**BMW**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/bmw/) — Luxury automotive. Dark premium surfaces, precise German engineering aesthetic
- [**Ferrari**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/ferrari/) — Luxury automotive. Chiaroscuro black-white editorial, Ferrari Red with extreme sparseness
- [**Lamborghini**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/lamborghini/) — Luxury automotive. True black cathedral, gold accent, LamboType custom Neo-Grotesk
- [**Renault**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/renault/) — French automotive. Vivid aurora gradients, NouvelR proprietary typeface, zero-radius buttons
- [**Tesla**](https://github.com/VoltAgent/awesome-design-md/tree/main/design-md/tesla/) — Electric vehicles. Radical subtraction, cinematic full-viewport photography, Universal Sans



## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

- **Improve existing files**: Fix wrong colors, missing tokens, weak descriptions
- **Report issues**: Let us know if something looks off

Before opening a PR, please [open an issue](https://github.com/VoltAgent/awesome-design-md/issues) first to discuss your idea and get feedback from maintainers.


## License

MIT License - see [LICENSE](LICENSE)

This repository is a curated collection of design system documents extracted from public websites. All DESIGN.md files are provided "as is" without warranty. The extracted design tokens represent publicly visible CSS values. We do not claim ownership of any site's visual identity. These documents exist to help AI agents generate consistent UI.
