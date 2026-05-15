# how-to-clone-website
AI website cloning with Claude Skills — clone any site structure using Claude Code

![Claude](https://img.shields.io/badge/Claude-Code-cc785c?style=flat&labelColor=555)
![Next.js](https://img.shields.io/badge/Next.js-14-black?style=flat&labelColor=555&logo=nextdotjs)
![Tailwind](https://img.shields.io/badge/Tailwind-CSS-38B2AC?style=flat&labelColor=555)
![Playwright](https://img.shields.io/badge/Playwright-Scraper-2EAD33?style=flat&labelColor=555)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat&labelColor=555)

[Concepts](#-concepts) · [How It Works](#️-how-it-works) · [Install](#-install) · [Workflow](#-workflow) · [Tips](#-tips-and-tricks-10) · [Startups](#️-startups--businesses)

---

## 🧠 CONCEPTS

| Feature | Location | Description |
|---------|----------|-------------|
| [**Claude Clone Skill**](skills/website-cloner/) | `skills/website-cloner/` | SKILL.md — tells Claude exactly how to clone any site |
| [**Playwright Scraper**](scraper/) | `scraper/scrape.py` | Captures DOM, CSS, assets, layout structure |
| [**Component Mapper**](mapper/) | `mapper/map.py` | Maps scraped HTML → React/Next.js components |
| [**Style Extractor**](extractor/) | `extractor/styles.py` | Extracts Tailwind-equivalent classes from computed CSS |
| [**Vercel Deploy**](deploy/) | `deploy/deploy.sh` | One command: build → optimize → deploy to Vercel |
| [**Legal Guard**](docs/) | `docs/legal.md` | Structure only — no copying proprietary content |

### 🔥 Hot

| Feature | Location | Description |
|---------|----------|-------------|
| [**One-prompt clone**](skills/website-cloner/) | Claude Code | "Clone [URL]" → full Next.js codebase in minutes |
| [**Structure-only**](skills/website-cloner/) | SKILL.md | Copies layout + UX pattern, not content — legally safe |
| [**Agency rate**](docs/) | Pricing | Clone + customize = $500–1,500 per site in 2hrs |

---

## ⚙️ HOW IT WORKS

```
"Clone https://example.com for my client"
         ↓
Playwright scrapes: DOM, CSS, fonts, layout, images
         ↓
Claude analyzes structure:
  ├── Section breakdown (Hero, Features, CTA, Footer)
  ├── Component hierarchy
  ├── Color palette extraction
  └── Typography system
         ↓
Component generation: React + Tailwind per section
         ↓
Next.js project assembled → npx vercel --prod
```

---

## 🚀 INSTALL

```bash
git clone https://github.com/hmzainjamil/how-to-clone-website
cd how-to-clone-website
pip install playwright && playwright install chromium
npm install
# In Claude Code:
# cp skills/website-cloner/SKILL.md ~/.claude/skills/website-cloner/
```

---

## 📋 WORKFLOW

| Step | Command | Output |
|---|---|---|
| 1. Scrape | `python3 scraper/scrape.py URL` | `scraped/[site]/` JSON |
| 2. Analyze | Claude: "Analyze scraped/[site]/" | Component map |
| 3. Build | Claude: "Build Next.js from component map" | `output/[site]/` |
| 4. Deploy | `bash deploy/deploy.sh` | Live Vercel URL |

---

## 💡 TIPS AND TRICKS (10)

[scraping](#tips-scraping) · [components](#tips-components) · [legal](#tips-legal) · [agency](#tips-agency)

<a id="tips-scraping"></a>■ **Scraping (3)**

| Tip | Source |
|-----|--------|
| Use `--wait 3000` flag for JS-heavy sites — wait for React hydration before capture | [HMZ](https://github.com/hmzainjamil) |
| Screenshot every section at 1440px viewport — Claude vision can analyze layout | [DigiMinds](https://github.com/hmzainjamil) |
| Extract CSS custom properties first — they reveal the full design system | [HMZ](https://github.com/hmzainjamil) |

<a id="tips-components"></a>■ **Components (3)**

| Tip | Source |
|-----|--------|
| Map sections → shadcn/ui components first — 80% of sites use standard patterns | [HMZ](https://github.com/hmzainjamil) |
| Framer Motion for Hero animations — clients always notice and love it | [DigiMinds](https://github.com/hmzainjamil) |
| 21st.dev for interactive elements — pre-built React components, no custom code needed | [HMZ](https://github.com/hmzainjamil) |

<a id="tips-legal"></a>■ **Legal (2)**

| Tip | Source |
|-----|--------|
| Clone structure + layout only — replace all text/images with client content | [HMZ](https://github.com/hmzainjamil) |
| Check robots.txt before scraping — honor disallow rules | [HMZ](https://github.com/hmzainjamil) |

<a id="tips-agency"></a>■ **Agency (2)**

| Tip | Source |
|-----|--------|
| "Inspired by [competitor]" pitch to clients — they immediately understand the quality level | [DigiMinds](https://github.com/hmzainjamil) |
| Charge $500 clone + $1,000 customization = $1,500 for 3hrs work = $500/hr | [HMZ](https://github.com/hmzainjamil) |

---

## ☠️ STARTUPS / BUSINESSES

| This Repo / Feature | Replaced |
|-|-|
| **Website cloning workflow** | [Webflow](https://webflow.com), [Framer](https://framer.com) — manual rebuilds |
| **Structure analysis** | [SimilarWeb](https://similarweb.com), [BuiltWith](https://builtwith.com) |
| **Component generation** | [GitHub Copilot](https://github.com/features/copilot), [v0.dev](https://v0.dev) |
| **One-command deploy** | [Netlify](https://netlify.com), [Railway](https://railway.app) |

---

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=hmzainjamil/how-to-clone-website&type=Date)](https://star-history.com/#hmzainjamil/how-to-clone-website&Date)

---

<div align="center">
Built by <a href="https://github.com/hmzainjamil">HMZ</a> · AI website cloning for agency workflows
</div>
