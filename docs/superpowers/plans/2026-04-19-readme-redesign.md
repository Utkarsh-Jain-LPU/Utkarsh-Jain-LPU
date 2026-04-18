# README Redesign Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rewrite the GitHub profile README with a modern, dynamic, recruiter-optimized design featuring typing animations, impact metrics, grouped tech badges, and personality sections.

**Architecture:** Single-file rewrite of `README.md` using GitHub-flavored Markdown + inline HTML limited to what GitHub actually renders (no `style` attributes — GitHub strips them). External services for dynamic elements: `readme-typing-svg.demolab.com` for typing animations, `shields.io` for badges, `leetcard.jacoblin.cool` for LeetCode stats.

**Tech Stack:** GitHub Markdown, shields.io, readme-typing-svg, leetcard.jacoblin.cool

---

## File Structure

- **Modify:** `README.md` — complete rewrite
- **Modify:** `.gitignore` — add `.superpowers/` entry
- **Keep (unreferenced):** `header.png`, `header.jpg` — no longer used but kept in repo
- **Keep (dormant):** `.github/workflows/readme-stats.yml` — no longer needed but harmless to keep

---

### Task 1: Add .superpowers/ to .gitignore

**Files:**
- Create: `.gitignore`

- [ ] **Step 1: Create .gitignore with .superpowers/ entry**

```
.superpowers/
```

Write this to `.gitignore` at the project root.

- [ ] **Step 2: Commit**

```bash
git add .gitignore
git commit -m "chore: add .superpowers/ to .gitignore"
```

---

### Task 2: Write README — Hero + About Me (Sections 1-2)

**Files:**
- Modify: `README.md` (full rewrite — start fresh)

- [ ] **Step 1: Write the Hero section**

Replace the entire contents of `README.md` with:

````markdown
<div align="center">

<a href="https://github.com/Utkarsh-Jain-LPU">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=4000&pause=1000&color=58A6FF&center=true&vCenter=true&random=false&width=600&lines=Hello+World%2C+I'm+Utkarsh+Jain+%F0%9F%91%8B" alt="Typing SVG" />
</a>

**`Software Engineer @ Salesforce | Backend Systems Architect | Graph Database Expert`**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/utkarshjainlpu/)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=flat&logo=gmail&logoColor=white)](mailto:utkarshjain7869@gmail.com)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat&logo=leetcode&logoColor=black)](https://leetcode.com/u/Utkarsh_Jain/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/Utkarsh-Jain-LPU)

</div>
````

- [ ] **Step 2: Add the About Me section**

Append to `README.md`:

````markdown

---

## About Me

Backend engineer with **5.5+ years** building high-performance systems at scale. I turn complex data problems into elegant graph architectures and squeeze every millisecond out of query execution. Currently building enterprise cloud infrastructure at **Salesforce**, previously shipped graph database solutions at **Informatica** for 5+ years.

```
> When I'm not coding, I'm exploring mountain roads on my bike, replaying Assassin's Creed, or vibing to 90s hits.
```
````

- [ ] **Step 3: Preview and commit**

```bash
git add README.md
git commit -m "feat: add hero typing animation and about me section"
```

---

### Task 3: Write README — Impact Metrics + Experience Timeline (Sections 3-4)

**Files:**
- Modify: `README.md` (append)

- [ ] **Step 1: Add Impact at a Glance section**

Append to `README.md`:

````markdown

---

## Impact at a Glance

<div align="center">

![400%](https://img.shields.io/badge/400%25-Query_Speed_Boost-58A6FF?style=for-the-badge)
![60%](https://img.shields.io/badge/60%25-Latency_Reduction-3FB950?style=for-the-badge)
![3x](https://img.shields.io/badge/3x-Throughput_Gain-F0883E?style=for-the-badge)
![30%](https://img.shields.io/badge/30%25-Memory_Optimized-A371F7?style=for-the-badge)

</div>
````

- [ ] **Step 2: Add Experience Timeline section**

Append to `README.md`:

````markdown

---

## Experience

### 🟢 Software Engineer @ Salesforce
**Mar 2026 - Present** &nbsp; [![CURRENT](https://img.shields.io/badge/CURRENT-3FB950?style=flat-square)](#)

- Building enterprise-scale cloud platform infrastructure
- Working with distributed systems and scalable architectures
- Contributing to next-generation backend services

---

### 🔵 Software Engineer @ Informatica
**Sep 2020 - Feb 2026** &nbsp; `5.5 years`

- Achieved **400% faster** Cypher query execution through deep query optimization
- Reduced memory usage by **30%** via advanced data structure tuning
- Decreased system latency by **60%** across critical data pipelines
- Improved data processing throughput by **3x**
- Architected enterprise job scheduler using Spring Boot & Quartz, handling thousands of scheduled tasks
- Built graph analytics platform on Neo4j serving multiple business units
- Led microservices architecture design for data processing pipelines
- 🏆 **Outstanding Project Contribution Award** (Q2 2023)

`Java` `Neo4j` `Spring Boot` `Quartz` `Microservices` `Cypher` `REST APIs`
````

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat: add impact metrics and experience timeline"
```

---

### Task 4: Write README — Tech Stack + Currently Learning (Sections 5-6)

**Files:**
- Modify: `README.md` (append)

- [ ] **Step 1: Add Tech Stack badges section**

Append to `README.md`:

````markdown

---

## Tech Stack

<div align="center">

**`LANGUAGES`**

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![Cypher](https://img.shields.io/badge/Cypher-008CC1?style=for-the-badge&logo=neo4j&logoColor=white)

**`FRAMEWORKS & TECHNOLOGIES`**

![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![Microservices](https://img.shields.io/badge/Microservices-FF6F00?style=for-the-badge&logo=moleculer&logoColor=white)
![REST API](https://img.shields.io/badge/REST_API-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Quartz](https://img.shields.io/badge/Quartz-000000?style=for-the-badge&logo=quartz&logoColor=white)

**`DATABASES`**

![Neo4j](https://img.shields.io/badge/Neo4j-008CC1?style=for-the-badge&logo=neo4j&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=for-the-badge&logo=elasticsearch&logoColor=white)

**`DEVOPS & TOOLS`**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white)
![Jira](https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white)

</div>
````

- [ ] **Step 2: Add Currently Learning section**

Append to `README.md`:

````markdown

---

## Currently Learning

<div align="center">

| ☁️ Cloud-Native Architecture | 🏗️ Distributed Systems | 📐 System Design Patterns | ⚡ Performance Engineering |
|:---:|:---:|:---:|:---:|

</div>
````

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "feat: add tech stack badges and currently learning section"
```

---

### Task 5: Write README — LeetCode, Fun Facts & CTA (Sections 7-9)

**Files:**
- Modify: `README.md` (append)

- [ ] **Step 1: Add LeetCode section**

Append to `README.md`:

````markdown

---

## LeetCode

<div align="center">

[![LeetCode Stats](https://leetcard.jacoblin.cool/Utkarsh_Jain?theme=dark&font=Fira%20Code&ext=heatmap)](https://leetcode.com/u/Utkarsh_Jain/)

</div>
````

- [ ] **Step 2: Add Beyond Code (Fun Facts) section**

Append to `README.md`:

````markdown

---

## Beyond Code

<div align="center">

| 🎮 **Gamer** | 🏍️ **Rider** | 🎵 **Music Lover** |
|:---:|:---:|:---:|
| Assassin's Creed fanatic | Mountain roads on two wheels | 90s hits on repeat |

</div>
````

- [ ] **Step 3: Add Let's Connect CTA section**

Append to `README.md`:

````markdown

---

<div align="center">

<a href="https://github.com/Utkarsh-Jain-LPU">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=22&duration=4000&pause=1000&color=58A6FF&center=true&vCenter=true&random=false&width=500&lines=Let's+build+something+amazing+together!+%F0%9F%9A%80" alt="Typing SVG" />
</a>

**Open to collaborations, architecture discussions, and new opportunities**

[![Email](https://img.shields.io/badge/utkarshjain7869@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:utkarshjain7869@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/utkarshjainlpu/)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/Utkarsh_Jain/)

---

```
> "Building scalable systems, one commit at a time" ⚡
```

</div>
````

- [ ] **Step 4: Commit**

```bash
git add README.md
git commit -m "feat: add leetcode stats, fun facts, and connect CTA"
```

---

### Task 6: Final Verification

- [ ] **Step 1: Read the full README.md and verify all sections are present**

Check that all 9 sections appear in order:
1. Hero (typing SVG + subtitle + flat social badges)
2. About Me (narrative + monospace hobbies)
3. Impact at a Glance (4 colored metric badges)
4. Experience (Salesforce with CURRENT badge + Informatica with metrics and tech tags)
5. Tech Stack (4 groups of for-the-badge badges)
6. Currently Learning (emoji table)
7. LeetCode (live card)
8. Beyond Code (fun facts table)
9. Let's Connect (typing SVG + contact badges + quote)

- [ ] **Step 2: Verify no references to removed elements**

Grep for these strings that should NOT appear:
- `header.png` — replaced by typing animation
- `komarev.com/ghpvc` — profile views counter removed
- `streak-stats.demolab.com` — streak card removed
- `profile/stats.svg` — stats card removed
- `profile/top-langs.svg` — top langs card removed

```bash
grep -E "header\.png|komarev|streak-stats|profile/stats|profile/top-langs" README.md
```

Expected: no output (no matches).

- [ ] **Step 3: Verify all external URLs are well-formed**

```bash
grep -oP 'https?://[^\s\)\]"]+' README.md | sort -u
```

Eyeball each URL for typos or malformed encoding.

- [ ] **Step 4: Final commit if any fixes were needed**

Only if changes were made during verification:

```bash
git add README.md
git commit -m "fix: address issues found during README verification"
```
