<h1 align="center">Awesome HTML Slide Skills</h1>

<p align="center"><i>The definitive list of agent skills and template libraries for generating beautiful, single-file HTML presentations — for Claude Code, Codex, Cursor, OpenClaw, and Hermes.</i></p>

<p align="center">
  <a href="LICENSE"><img alt="License: CC BY 4.0" src="https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg"></a>
  <a href="https://tosea.ai"><img alt="Made by Tosea.ai" src="https://img.shields.io/badge/Made%20by-Tosea.ai-000000?style=flat"></a>
  <a href="https://github.com/ToseaAI/awesome-html-slide-skills/stargazers"><img alt="GitHub stars" src="https://img.shields.io/github/stars/ToseaAI/awesome-html-slide-skills?style=flat&color=yellow"></a>
  <a href="https://github.com/ToseaAI/awesome-html-slide-skills/network/members"><img alt="GitHub forks" src="https://img.shields.io/github/forks/ToseaAI/awesome-html-slide-skills?style=flat&color=blue"></a>
  <a href="https://awesome.re"><img alt="Awesome" src="https://awesome.re/badge-flat2.svg"></a>
</p>

<p align="center"><b>English</b> · <a href="README.zh-CN.md">中文</a></p>

A curated, open-source list of **HTML slide generation skills** — packaged agent skills (Claude Code / Codex / Hermes / OpenClaw) and template libraries that turn one prompt, outline, or markdown file into a polished, zero-dependency, single-file HTML presentation.

Every entry below is a real, publicly available GitHub repository. Stars are pulled fresh from the GitHub API and used as the sole ordering signal. Descriptions and feature highlights are drawn from each project's own README and refined for consistency.

> **Maintained by [Tosea.ai](https://tosea.ai)** — we build AI-native presentation tooling. If you ship an HTML slide skill or template library, [open a PR](CONTRIBUTING.md) and we'll add it.

---

## Contents

- [About this list](#about-this-list)
- [Skills](#skills)
  - [Tier S · Foundational / 1k+ stars](#tier-s--foundational--1k-stars)
  - [Tier A · Production-ready / 100–1000 stars](#tier-a--production-ready--1001000-stars)
  - [Tier B · Emerging / specialized](#tier-b--emerging--specialized)
- [Templates](#templates)
- [Contributing](#contributing)
- [License](#license)

---

## About this list

**What counts as an "HTML slide skill"?**

A skill is a self-contained package — usually a `SKILL.md`, a folder of reference styles, and a small runtime — that an AI coding agent can load to produce a finished HTML deck. Most projects below target Claude Code's [Agent Skills](https://docs.claude.com/en/docs/claude-code/skills) format, but many are agent-agnostic and work with Codex, Cursor, OpenClaw, Hermes, or anything that can read a markdown instruction file.

**Skills vs. templates.**

- **Skills** (the primary focus of this list) are *generative*: the agent writes the deck from your prompt, your outline, or your document, picking layouts and themes intelligently. They include planning logic, content-routing rules, anti-AI-slop checks, and full design systems.
- **Templates** are *static*: hand-crafted HTML/CSS scaffolds you (or an agent) can copy and fill in. Smaller in scope, but extremely useful as the visual ground truth that skills reference.

**Why this list exists.**

HTML decks have quietly become the format of choice for AI-generated presentations: they render anywhere, embed anything, version-control cleanly, and never crash a board meeting because PowerPoint couldn't find a font. The ecosystem exploded in early 2026 — we counted 20+ serious skill packages in two months — but no one had collected them in one place. This is that place.

---

## Skills

> Ordered by GitHub star count, descending. Star counts last refreshed 2026-05-13.
> The tier cutoffs are heuristics, not value judgments — a 24-star skill targeting Huawei-style decks is probably more useful for that use case than a 17k-star generalist.

### Tier S · Foundational / 1k+ stars

These are the projects most of the others reference, fork, or benchmark against. If you're new to HTML slide skills, start here.

---

#### 1. [zarazhangrui/frontend-slides](https://github.com/zarazhangrui/frontend-slides) · ⭐ 17,262

> Create beautiful slides on the web using Claude's frontend skills.

The project that kicked off the modern HTML-slide-skill wave. Built on a "show, don't tell" philosophy: instead of asking you to describe your aesthetic preferences in words, it generates visual previews and lets you pick what you like. Designed so non-designers can produce decks without ever touching CSS or JavaScript.

**Themes (16, grouped by feel)**

- **Dark** — Bold Signal (vibrant card on dark), Electric Studio (clean split-panel), Creative Voltage (retro-modern electric blue + neon), Dark Botanical (elegant with warm accents).
- **Light** — Notebook Tabs (editorial, paper with colorful tabs), Pastel Geometry (vertical pills, friendly), Split Pastel (playful two-color vertical split), Vintage Editorial (witty, geometric shapes).
- **Specialty** — Neon Cyber (particle bg, neon glow), Terminal Green (hacker aesthetic), Swiss Modern (Bauhaus-inspired), Paper & Ink (drop caps and pull quotes).

**Why it stands out**: ergonomic style-discovery flow, a healthy fork ecosystem (see `frontend-slides-editable` below), and Anthropic itself uses the project as an example of what skills can do.

---

#### 2. [nicobailon/visual-explainer](https://github.com/nicobailon/visual-explainer) · ⭐ 8,163

> Agent skill that generates rich HTML pages or slide decks for diagrams, diff reviews, plan audits, data tables, and project recaps.

A "Swiss army knife" skill — it'll happily produce a single landing page, a code-walkthrough deck, or a 40-slide project recap. Especially strong on technical content: diff reviews, plan audits, and inline SVG diagrams.

**Aesthetics (4, dark-first by default)**

- **Midnight Editorial** — Deep navy, serif display, warm gold accents. Bloomberg Businessweek meets Apple keynote.
- **Terminal Mono** — Dark background, monospace everything, green/cyan accents. Developer-native deep-dives.
- **Warm Signal** — Cream paper background, bold sans, terracotta/coral cards. Pitches and overviews.
- **Swiss Clean** — White, geometric sans, single accent color, visible grid. Data-heavy analytical content.

---

#### 3. [op7418/guizang-ppt-skill](https://github.com/op7418/guizang-ppt-skill) · ⭐ 7,942

> A Claude Code Skill that turns prompts into horizontal-swipe magazine-style HTML decks — 10 layouts, 5 curated themes, WebGL hero backgrounds, single-file output.

The "magazine voice" of the ecosystem. Two flagship styles you'll recognize on sight:

- **Style A — 电子杂志 × 电子墨水**. Monocle meets code. Narrative, opinion, sharing, personal-voice talks.
- **Style B — 瑞士国际主义**. Grid-first, single high-saturation anchor color, hairline rules, extreme type-scale contrast. Product launches, analysis, methodology.

**Fits**: offline sharing, industry-internal talks, private salons, AI product launches, demo day, speaker-led personal-style talks.
**Doesn't fit**: dense tabular data, training materials (too low-density), real-time collaborative editing (static HTML).

---

#### 4. [lewislulu/html-ppt-skill](https://github.com/lewislulu/html-ppt-skill) · ⭐ 3,582

> HTML PPT Studio — A world-class AgentSkill for producing professional HTML presentations.

By far the most feature-loaded skill on this list. Pure static HTML/CSS/JS, no build step, true presenter mode with pixel-perfect previews + speaker script + timer.

- **36 themes** — `minimal-white`, `editorial-serif`, `soft-pastel`, `arctic-cool`, `catppuccin-latte`, `catppuccin-mocha`, `dracula`, `tokyo-night`, `nord`, `solarized-light`, `gruvbox-dark`, `rose-pine`, `neo-brutalism`, `glassmorphism`, `bauhaus`, `swiss-grid`, `xiaohongshu-white`, `aurora`, `blueprint`, `memphis-pop`, `cyberpunk-neon`, `y2k-chrome`, `retro-tv`, `japanese-minimal`, `vaporwave`, `midcentury`, `corporate-clean`, `academic-paper`, `news-broadcast`, `pitch-deck-vc`, `magazine-bold`, `engineering-whiteprint`, and more.
- **15 full-deck templates** — 8 extracted from real-world decks (`xhs-white-editorial`, `graphify-dark-graph`, `knowledge-arch-blueprint`, `hermes-cyber-terminal`, `obsidian-claude-gradient`, `testing-safety-alert`, `xhs-pastel-card`, `dir-key-nav-minimal`) plus 7 scenario decks (`pitch-deck`, `product-launch`, `tech-sharing`, `weekly-report`, `xhs-post` 9-slide 3:4, `course-module`, `presenter-mode-reveal` 🎤 with 150–300 word speaker scripts on every slide).
- **31 page layouts**, **47 animations** (27 CSS + 20 canvas FX), **presenter mode with the `S` key**.

---

#### 5. [zarazhangrui/beautiful-html-templates](https://github.com/zarazhangrui/beautiful-html-templates) · ⭐ 1,037

> A library of HTML slide templates designed so any coding agent can pick the right one and produce a beautiful deck on the user's behalf, automatically.

Sibling repo to `frontend-slides` — pure templates, no skill logic. 32 templates, 3 slides each (cover · mid-deck · later) so an agent can see how each visual system actually handles different layout duties before committing.

Also listed under [Templates](#templates) below.

---

### Tier A · Production-ready / 100–1000 stars

Mature, actively maintained skills with a clear style point of view. Best when you know roughly what you want — e.g. "I need a McKinsey-style consulting deck" — and want a skill that does *only* that, well.

---

#### 6. [mucsbr/ppt-agent-workflow-san](https://github.com/mucsbr/ppt-agent-workflow-san) · ⭐ 517

> 渐进交互式 PPT 生成 skill — progressive interactive PPT generation.

Two-stage workflow split across sub-repos:

- `ppt-workflow/` — generates PPT content plans and exports HTML or PNG previews.
- `html-slide-to-pptx/` — converts structured HTML slides into editable PPTX.

Notable for treating the HTML→PPTX export problem as a first-class concern, not an afterthought.

---

#### 7. [vigorX777/ppt-svg-generator](https://github.com/vigorX777/ppt-svg-generator) · ⭐ 216

> Skill that converts Markdown into HTML/PDF presentations with multiple preset styles.

| Style | Character | Use case |
| --- | --- | --- |
| 极简主义 | Pure white, lots of whitespace, Klein-blue accents | Product launches, design sharing, TED talks |
| 商务咨询 | Deep blue, McKinsey-style, orange emphasis | Proposals, consulting reports, investor pitches |
| 科技暗黑 | Dark background, neon gradients, glassmorphism | Tech sharing, product demos, hackathons |
| 瑞士平面 | High contrast, Bauhaus, signal red | Creative pitches, brand showcases |
| 品牌蓝 | Blue-purple-cyan palette, modern professional | Corporate training, formal presentations |

---

#### 8. [bbostaice/axi-front-design-skill](https://github.com/bbostaice/axi-front-design-skill) · ⭐ 188

> A Claude Code Skill that makes Claude act as a senior designer — landing pages, slide decks, interactive prototypes, motion demos, infographics, mobile mockups.

**Key behaviors**

- Asks questions before building (via popup, not lists).
- Reads real design tokens from your codebase instead of guessing.
- Delivers 3+ variants across different visual/interaction dimensions.
- Avoids AI design clichés (gradients-for-the-sake-of-it, emoji-stuffing, Lorem-Ipsum filler sections).

---

#### 9. [likaku/Mck-ppt-design-skill](https://github.com/likaku/Mck-ppt-design-skill) · ⭐ 133

> Consulting firm–style PowerPoint design system for AI agents. 70 layout patterns, flat design, python-pptx. 麦麸风格 PPT 设计系统。

AI-native PowerPoint design system — 67 layouts · Harness Engineering · BLOCK_ARC charts · QA pipeline · Python runtime. The most opinionated McKinsey/BCG-style skill in the list; outputs lean PPTX rather than HTML, useful when the audience expects a `.pptx` file but you want consulting-grade typography.

---

#### 10. [archlizheng/frontend-slides-editable](https://github.com/archlizheng/frontend-slides-editable) · ⭐ 124

> Editable HTML presentation skill for Codex/Claude Code with drag-resize editing, slide reordering, local save/export, and PPTX-to-web conversion.

Editable fork of `zarazhangrui/frontend-slides`. Keeps the upstream style discovery, viewport discipline, and PPT conversion, then adds a full in-browser editing runtime: drag objects, resize blocks, edit text, reorder slides, save locally, export a clean standalone HTML.

> Real decks should still implement each preset's signature layout from `STYLE_PRESETS.md`. Edit mode is an add-on, not permission to reuse a generic slide prototype for every aesthetic.

---

### Tier B · Emerging / specialized

Smaller star counts, but several of these are the *best* option for their niche — Huawei-style strategy decks, knowledge-retention teaching slides, anti-AI-slop design tokens, etc.

---

#### 11. [bytonylee/future-slide-skill](https://github.com/bytonylee/future-slide-skill) · ⭐ 80

> Reusable slide-generation skill for image-based and HTML-based AI workflows.

One of the few skills designed to switch cleanly between image-rendered slides (e.g. for social media carousels) and live HTML decks from the same content IR.

---

#### 12. [edu-ai-builders/visual-cognition-slides](https://github.com/edu-ai-builders/visual-cognition-slides) · ⭐ 55

> An HTML slide design skill grounded in cognitive science and instructional design. Outputs presentation decks optimized for knowledge retention.

Every decision — narrative structure, per-slide layout, animation choice — answers a single question: *what cognitive action does the audience need to perform here?*

**Best for**: teachers, researchers, PhD students, content creators (voice-over videos, knowledge channels), internal training and talks.
**Not for**: pure commercial decks (PowerPoint / Keynote ship faster), real-time collaborative editing (use Google Slides).

---

#### 13. [WayneZhon/KingDee-PPT-Skill](https://github.com/WayneZhon/KingDee-PPT-Skill) · ⭐ 45

> 将文字、大纲、文档一键转换为金蝶官方风格 .pptx 或交互式 HTML 幻灯片。

Fully reproduces the 2026 official Kingdee International template design language. Dual-style system (Classic / Bento Motion), 29 layouts, 7 auto-detected thinking models, embedded official background and logo, zero-config.

---

#### 14. [kaisersong/slide-creator](https://github.com/kaisersong/slide-creator) · ⭐ 37

> A skill for Claude Code and OpenClaw that generates stunning, zero-dependency HTML presentations.

- **IR-first workflow** — `--plan` distills `BRIEF.json`, `--generate` renders from the IR.
- **Two planning depths** — Auto for speed, Polish for narrative + visual locking.
- **Content Review System** — 16 checkpoints; `--review` for on-demand diagnosis; Polish auto-runs review; three rule types (hard / context-aware / advisory).
- **22 design presets** with named layout variations.
- **Content-type routing** — auto-suggests best style for pitch decks, dev tools, data reports.
- **Style discovery** — 3 visual previews before committing.
- **Inline SVG diagrams** — flowcharts, timelines, bar charts, comparison grids, org charts. No external libs.
- **"Blue Sky" starter template** so models never mis-implement the visual system.

---

#### 15. [software-ai-life/Awesome-PPT-Design-Skills](https://github.com/software-ai-life/Awesome-PPT-Design-Skills) · ⭐ 36

> Agent-agnostic PPT design skills for generating polished PowerPoint decks with [ppt-master](https://github.com/hugohe3/ppt-master).

Meta-collection rather than a single skill. The author packages multiple distinct visual systems (`japanese-style-ppt-skill`, `soft-3d-clay-ppt-skill`, `futuristic-tech-editorial-ppt-skill`, `minimalist-luxury-branding-ppt-skill`, `modern-illustration-editorial-ppt-skill`, `japanese-hand-drawn-editorial-ppt-skill`) and ships them as a stable visual layer for whichever coding agent you happen to use (Codex, Claude Code, Cursor, OpenCode, OpenClaw, Hermes). Traditional Chinese decks are first-class.

Also listed under [Templates](#templates) below.

---

#### 16. [Akxan/ppt-agent-skill](https://github.com/Akxan/ppt-agent-skill) · ⭐ 33

> World-class AI presentation generator · 26 styles · 18 charts · benchmarked against Linear / Anthropic / Stripe / Apple / NYT.

Models a full agency workflow rather than "outline → template": research first, content drives layout, global style stays consistent, real data fills placeholders. Visual fidelity is benchmarked against actual production CSS of brands like Linear and Anthropic — not screenshots, the real implementations.

**Style families**

- 暗色专业 — 7 styles (`references/styles/dark.md`)
- 浅色高级 — 8 styles (`references/styles/light.md`)
- 活力鲜明 — 4 styles (`references/styles/vibrant.md`)
- 东方文化 — 3 styles (`references/styles/cultural.md`)
- 自然/复古 — 4 styles (`references/styles/natural.md`)

---

#### 17. [FeeiCN/slide-writer](https://github.com/FeeiCN/slide-writer) · ⭐ 32

> A slide-writing skill that generates enterprise HTML presentations from ideas, outlines, documents, and speech drafts.

- **Any input → enterprise-grade deck** — sentence, outline, speech draft, notes, existing HTML.
- **14 brand themes, auto-detected** — Ant Group, Alibaba, Tencent, ByteDance and more. Mention the keyword, the right theme/logo/colors load automatically.
- **Single-file delivery** — one standalone HTML; CSS, JS, images all embedded. Opens in any browser.
- **Always up to date** — pulls latest themes, components, and generation rules on every run.

---

#### 18. [zuiho-kai/huawei-style-ppt-skill](https://github.com/zuiho-kai/huawei-style-ppt-skill) · ⭐ 24

> 华为风格 PPT Skill — high-density information PPT workflow.

End-to-end workflow specifically tuned for Huawei-style strategy pages, architecture overviews, data insights, and side-by-side solution comparisons — i.e. document-style high-density decks that are intentionally heavier than a typical slide.

---

#### 19. [Phlegonlabs/Powerpoint-fancy-design](https://github.com/Phlegonlabs/Powerpoint-fancy-design) · ⭐ 23

> A presentation-design skill for Codex and Claude Code that turns page-structured Markdown into styled 1600x900 HTML slides, PNG renders, and exportable PPTX decks.

**Use it for**:

- Business and policy decks needing disciplined hierarchy and presentation-safe typography.
- Brand / culture / exhibition decks needing stronger visual direction than stock templates.
- Chinese and bilingual decks needing style-aware font pairing instead of generic fallbacks.
- Static HTML-to-PPT workflows where final visual fidelity matters more than editable PPT primitives.

---

#### 20. [xhshow2025/-PPT-sense-deck-skill-](https://github.com/xhshow2025/-PPT-sense-deck-skill-) · ⭐ 18

> 鲸格 PPT — a Codex Skill for generating high-quality browser-native presentations.

Static HTML/CSS/JS output with a complete pipeline: content IR, theme system, full deck templates, single-page layouts, animation runtime, presenter mode, editable mode, gesture controls, export helpers.

**Distinctive themes**

- `apple-bento-glass` — AI / product strategy / new-category launches.
- `executive-clean` — board reports, strategy updates, investor updates, weekly reports.
- `semantic-dark` — tech sharing, architecture walkthroughs, AI systems, developer demos.
- `xhs-editorial` — Xiaohongshu image-text, social carousels, consumer education.
- `cyber-neon` — Demo Day, RGB hardware, cyberpunk launches.
- `warm-paper` — courses, lecture notes, stories, cultural themes.
- `nordic-childrens-picture-book` — Nordic children's-book nostalgia and humor.
- 史诗级 — historical cultural narratives, 昭君出塞, Chinese cinematic feel.
- `neon-noir-city` — cyberpunk city, AI future life, 2098-style narratives.

---

#### 21. [nghiahsgs/skills-slides](https://github.com/nghiahsgs/skills-slides) · ⭐ 17

> 50,000+ unique HTML presentation designs. Zero dependencies. Anti-AI-slop. A Claude Code skill.

Fights AI-generated mediocrity with a **token-based design system** and a strict **anti-slop checklist** that catches generic patterns *before* the deck is delivered. Result: decks that look intentionally designed, not template-generated.

- **Aesthetics (50)** — `startup-pitch`, `neon-cyber`, `editorial-minimal`, `luxury-noir`, `consulting-swiss`, `vaporwave`, `terminal-hacker`, `ai-ml-showcase`, and more. Each defines compatible palettes, fonts, layouts, and signature effects.
- **Palettes (20)** — `midnight-aurora`, `crimson-signal`, `electric-indigo`, `rose-gold`, `arctic-frost`, `carbon-fiber`, etc. WCAG contrast ratios shipped for every palette.
- **Fonts (10)** — Display + body pairs from Google Fonts and Fontshare (`clash-satoshi`, `fraunces-worksans`, `syne-spacemono`, `bodoni-dmsans`).
- **Effects (30+)** — full CSS+JS snippets with performance impact tagged: `particle-bg`, `gradient-mesh`, `aurora-flow`, `grid-overlay`, `glassmorphism`, `noise-texture`, `magnetic-cursor`.

---

#### 22. [codesstar/next-slide](https://github.com/codesstar/next-slide) · ⭐ 17

> 你的下个 slide，何必是 PPT — AI-powered HTML presentations. 26+ styles, zero dependencies, bilingual. Works with Claude Code & OpenClaw, Hermes Agent.

Each style is a complete design system: curated typography, color palette, layout patterns, signature animations, responsive breakpoints.

| Category | Count | Styles | Vibe |
| --- | --- | --- | --- |
| Dark | 11 | Keynote Noir, Bold Signal, Neon Cyber, Terminal Green, Midnight Corporate, Cinema Scope, Dark Botanical, Starfield, Dark Premium, Dark Cinema, Futuristic Blue | Conferences, launches, tech talks |
| Light | 11 | Swiss Modern, Paper & Ink, Notebook Tabs, Pastel Geometry, Morning Brief, Campus White, Soft Landing, Watercolor Wash, Korean Soft, Claymorphism 3D, Wabi-Sabi Zen | Academic, business, teaching |
| Editorial | 4 | Editorial Serif, Fashion Editorial, Newsprint Broadsheet, Vintage Editorial | Magazine layouts, thought leadership |
| Bold | 7 | Electric Studio, Creative Voltage, Split Pastel, Pop Art, Bold Typography, Neon Brutalism, Memphis Pop | Startups, creative pitches |
| Retro | 5 | Grainy Retro, Art Deco Gatsby, Risograph Overprint, Vintage Poster, Retro Arcade | Nostalgic, stylized |
| Artistic | 7 | Surrealism Gallery, Scrapbook Portfolio, Blue Collage, Pink Handwritten, Art Nouveau Botanical, Soft Dreamy, Terracotta Earth | Art, design, portfolio |
| Cultural | 8 | 东方墨韵, 和風, Gradient Dreams, Blueprint, Bauhaus Primary, Swiss Grid, Aurora Mesh, Chinese Ink Wash | Cultural events, themed talks |

---

## Templates

Hand-crafted HTML template libraries — drop them into a project, point your agent at the folder, get a deck.

---

#### T1. [zarazhangrui/beautiful-html-templates](https://github.com/zarazhangrui/beautiful-html-templates) · ⭐ 1,037

> A library of HTML slide templates designed so any coding agent can pick the right one and produce a beautiful deck on the user's behalf, automatically.

**32 templates**, three slides per template (cover · mid-deck · later) to show how each visual system handles different layout duties. The de-facto reference template library for the Claude Code skill ecosystem — many skills above will pull from or reference these templates directly.

---

#### T2. [software-ai-life/Awesome-PPT-Design-Skills](https://github.com/software-ai-life/Awesome-PPT-Design-Skills) · ⭐ 36

> Agent-agnostic PPT design skills, distributed as a library of style packs.

Acts as a multi-style template library when you don't want to commit to one aesthetic:

- **japanese-style-ppt-skill** — 日本風格高端編輯簡報 with two house styles:
  - *Washi Paper & Soft Glow* — 和紙感米白背景, 柔和微光與低彩度色系, 細灰線、靛藍克制點綴, 大量留白但有溫度.
  - *Japanese Lifestyle Editorial* — 純白背景, 焦橙與深炭灰, 高端生活雜誌式排版, 非對稱壓邊圖片與結構化 grid.
- **soft-3d-clay-ppt-skill** — Claymorphism. 暖米色 `#FDF5E6`, 鼠尾草綠 `#B2AC88`, 莫蘭迪粉 `#DBADAD`, 柔霧感幾何形狀.
- **futuristic-tech-editorial-ppt-skill** — Futuristic tech editorial. 純白 `#FFFFFF`, 電光藍 `#2F6BFF`, 石墨灰 `#2B2B2B`, 細線 grid, 資料感模組, 平面銳利.
- **minimalist-luxury-branding-ppt-skill** — High-end brand proposal. 暖米色 `#F5EFE6`, 柔棕色 `#A68A64`, 深灰文字 `#3A3A3A`, 襯線標題 + 無襯線內文, 精品感節奏.
- **modern-illustration-editorial-ppt-skill** — Modern illustration editorial. 柔米色 `#F7F3EE`, 霧藍 `#A7C7E7`, 灰橘 `#E8A87C`, 炭灰 `#2F2F2F`, 柔和向量插畫.
- **japanese-hand-drawn-editorial-ppt-skill** — Japanese hand-drawn editorial. 暖白紙感 `#F8F6F2`, 墨黑線條 `#2B2B2B`, 柔灰 `#BDBDBD`, 低彩靛藍 `#6C7A89`, 鉛筆/墨線插畫 + 淡水彩.

---

## Contributing

PRs welcome — see [CONTRIBUTING.md](CONTRIBUTING.md). The bar:

1. Repo must be public, MIT/Apache/CC-style licensed, and contain real working code (a skill manifest or a template directory — not just a README).
2. Output must be HTML-first (PPTX export is fine as long as HTML is the source of truth).
3. Star count is checked at PR merge time and used to place the entry in the right tier.

If you find a broken link, a stale star count, or a project we missed, [open an issue](https://github.com/ToseaAI/awesome-html-slide-skills/issues/new).

---

## License

Curated content (this README, the structure, the descriptive text) is licensed under [CC BY 4.0](LICENSE). Each linked project retains its own license — check the linked repos before reuse.

---

<p align="center">
  Maintained by <a href="https://tosea.ai"><b>Tosea.ai</b></a> · <a href="https://github.com/ToseaAI/awesome-gpt-image-2-prompts">Also see: awesome-gpt-image-2-prompts</a>
</p>
