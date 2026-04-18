# GitHub Profile README Redesign — Design Spec

## Goals

- **Primary**: Attract recruiters/hiring managers — impact metrics front-and-center, scannable in 10 seconds
- **Secondary**: Personal brand / networking hub — memorable, personality-rich, drives connections
- **Vibe**: Modern & dynamic + bold & creative. Dark-theme native, typing animations, standout layout

## Full Section Breakdown

### 1. Hero / Intro

- **Typing animation** via `readme-typing-svg` (demolab.com): `"Hello World, I'm Utkarsh Jain"` with blinking cursor, Fira Code font, color `#58A6FF`
- **No banner image** — the typing effect replaces `header.png`
- **Subtitle**: `Software Engineer @ Salesforce | Backend Systems Architect | Graph Database Expert`
- **Social badges**: LinkedIn, Gmail, LeetCode, GitHub — `flat` style (not `for-the-badge`) for compactness
- **Remove** profile views counter

### 2. About Me

- 2-3 line narrative paragraph. Content:
  > Backend engineer with **5.5+ years** building high-performance systems at scale. I turn complex data problems into elegant graph architectures and squeeze every millisecond out of query execution. Currently building enterprise cloud infrastructure at **Salesforce**, previously shipped graph database solutions at **Informatica** for 5+ years.
- Fun facts line in monospace/terminal style:
  > `> When I'm not coding, I'm exploring mountain roads on my bike, replaying Assassin's Creed, or vibing to 90s hits.`

### 3. Impact at a Glance

A horizontal row of 4 bold metric tiles (implemented as inline HTML `<div>` blocks with colored borders — Markdown tables can't do colored styling):

| Metric | Value | Color |
|--------|-------|-------|
| Query Speed Boost | 400% | Blue `#58A6FF` |
| Latency Reduction | 60% | Green `#3FB950` |
| Throughput Gain | 3x | Orange `#F0883E` |
| Memory Optimized | 30% | Purple `#A371F7` |

### 4. Experience Timeline

Vertical timeline using inline HTML with a left-border line, colored dot indicators, and inline `<strong>` tags for metrics. Pure Markdown can't do a visual timeline, so this section uses an HTML block:

**Salesforce — Software Engineer (Mar 2026 - Present)**
- Green circle indicator + `CURRENT` badge
- Bullets: enterprise-scale cloud platform, distributed systems, scalable architectures

**Informatica — Software Engineer (Sep 2020 - Feb 2026 · 5.5 years)**
- Blue circle indicator
- Bullets with color-coded metrics inline:
  - 400% faster Cypher query execution
  - 30% memory reduction
  - 60% latency decrease
  - Enterprise job scheduler (Spring Boot & Quartz)
  - Graph analytics platform on Neo4j
  - Microservices architecture for data pipelines
- Tech tags at bottom: `Java` `Neo4j` `Spring Boot` `Quartz` `Microservices`

### 5. Tech Stack (Badges)

Center-aligned badge rows grouped with colored category labels:

- **Languages** (blue label): Java, C++, JavaScript, SQL, Cypher
- **Frameworks & Technologies** (green label): Spring Boot, Microservices, REST API, Quartz
- **Databases** (orange label): Neo4j, MongoDB, MySQL, Elasticsearch
- **DevOps & Tools** (purple label): Docker, Jenkins, Git, Maven, Jira

All badges use `for-the-badge` style from shields.io.

### 6. Currently Learning

Compact emoji + label grid, center-aligned:

- ☁️ Cloud-Native Architecture
- 🏗️ Distributed Systems
- 📐 System Design Patterns
- ⚡ Performance Engineering

### 7. LeetCode

Live-updating LeetCode stats card using `leetcard.jacoblin.cool` with:
- Dark theme
- Username: `Utkarsh_Jain`
- Compact layout

### 8. Beyond Code (Fun Facts)

3 mini cards in a row (inline HTML `<div>` blocks with border styling to match the dark theme):

| 🎮 Gamer | 🏍️ Rider | 🎵 Music Lover |
|-----------|-----------|----------------|
| Assassin's Creed fanatic | Mountain roads on two wheels | 90s hits on repeat |

### 9. Let's Connect (CTA)

- Second typing animation: `"Let's build something amazing together!"`
- One-liner: "Open to collaborations, architecture discussions, and new opportunities"
- Contact links as styled badges: Email, LinkedIn, LeetCode
- Signature quote in terminal style: `> "Building scalable systems, one commit at a time" ⚡`

## Removed from Current README

- `header.png` banner image (replaced by typing animation)
- Profile views counter (low counts hurt perception)
- GitHub stats cards, top languages, streak stats (public stats don't reflect enterprise work)
- Key Achievements table (redundant — metrics now embedded in experience timeline and impact tiles)
- Redundant contact section (consolidated into CTA)

## Implementation Notes

- The README will be GitHub-flavored Markdown + inline HTML for sections that need visual styling (metric tiles, experience timeline, fun fact cards). GitHub renders inline HTML in READMEs but strips `<style>` tags and most JS — all styling must be inline `style` attributes.
- Typing SVGs come from `readme-typing-svg.demolab.com` — no local assets needed
- LeetCode card from `leetcard.jacoblin.cool` — no local assets needed
- The `header.png` and `header.jpg` files can be kept in repo but won't be referenced
- GitHub Actions workflow (`readme-stats.yml`) can be removed or kept dormant since we're dropping stats cards
- `.superpowers/` directory should be added to `.gitignore`

## Section Order (Top to Bottom)

1. Hero (typing animation + subtitle + social badges)
2. About Me (narrative + hobbies)
3. Impact at a Glance (metric tiles)
4. Experience Timeline (Salesforce + Informatica)
5. Tech Stack (grouped badges)
6. Currently Learning (emoji grid)
7. LeetCode (live card)
8. Beyond Code (fun fact cards)
9. Let's Connect (CTA + typing animation + contact badges + quote)
