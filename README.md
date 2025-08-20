# web-assistent

A modern, multi‑device web assistant for the Italian primary school mathematics curriculum. Built with semantic HTML5, responsive CSS, and vanilla JavaScript, it delivers clear explanations, step‑by‑step solutions, and auto‑generated practice exercises powered by JSON datasets organized by grade (prima → quinta).

---

## Overview

- **Purpose:** Deliver a focused, distraction‑free math companion aligned to the Italian elementary curriculum, starting in Italian and expanding to English next.
- **Scope:** Full primary program coverage, organized into five JSON files (one per grade). Topics include numbers, operations, problem solving, geometry, measurement, and logic.
- **Format:** One professional, SEO‑ready index.html with a clean header/footer layout, accessible UI components, and responsive behavior across phones, tablets, and desktops.
- **Approach:** No frameworks, no build step. Standards‑based, maintainable, and easy to host on any static server or GitHub Pages.

---

## Key Features

- **Single page:** index.html as the core UX surface with a polished header, content panel, and footer.
- **Responsive UI:** CSS Grid/Flexbox layout for fluid scaling from 320px to wide screens; mobile‑first breakpoints.
- **Accessibility:** WCAG 2.1 AA‑minded color contrast, keyboard navigation, skip links, landmarks, ARIA labels.
- **SEO‑ready:** Descriptive metadata, canonical URL, Open Graph/Twitter cards, JSON‑LD schema, sitemap, robots.
- **Curriculum data:** Five grade‑specific JSON files with explanations, examples, and graded exercises.
- **Exercise engine:** Deterministic and random exercise generation, inline hints, and solution checking.
- **Statefulness:** Query parsing, topic routing, progress tracking (in‑memory; optional localStorage).
- **Dark mode:** Prefers‑color‑scheme integration with a manual toggle for user choice.
- **Offline‑friendly:** Static assets only; easy to extend to PWA if needed.

---

## Core Components

| Component | Purpose | Status | Notes |
|---|---|---|---|
| index.html | UI shell, semantic structure, SEO | Planned | Header, main chat/learning pane, footer |
| /assets/css/styles.css | Responsive layout, themes | Planned | Grid/Flex, dark/light, reduced motion |
| /assets/js/app.js | Routing, rendering, logic | Planned | Topic search, exercise engine, scoring |
| /assets/js/i18n.js | Localization utilities | Planned | Italian default; English upcoming |
| /data/grade-1.json | Prima (Grade 1) data | Planned | Numbers 0–100, add/sub, shapes, time |
| /data/grade-2.json | Seconda (Grade 2) data | Planned | Larger numbers, tables, money, length |
| /data/grade-3.json | Terza (Grade 3) data | Planned | Multiplication/division mastery, area |
| /data/grade-4.json | Quarta (Grade 4) data | Planned | Fractions, multi‑step problems, angles |
| /data/grade-5.json | Quinta (Grade 5) data | Planned | Decimals, percentages, perimeter/area |

> Sources: Concept structure and scope definition by the repository author.

---

## UX and Content Standards

- **Semantic structure:** Header, nav, main, aside, footer, and section/article where appropriate.
- **Forms and inputs:** Labels, descriptions, error states, and accessible focus order.
- **Copy style:** Short, student‑friendly explanations; consistent terminology across grades.
- **Assessment:** Instant feedback, step‑wise solutions, and gentle remediation hints.
- **Visual design:** Neutral palette, high contrast, spacious line‑height, and iconography with text.

---

## SEO and Social Sharing

- **Meta:** Title (<60 chars), description (150–160 chars), canonical URL.
- **Open Graph:** og:title, og:description, og:type=website, og:image, og:url.
- **Twitter Cards:** summary_large_image with mirrored OG content.
- **Structured data:** JSON‑LD (WebSite, Organization, and BreadcrumbList patterns).
- **Indexing:** robots.txt (allow), sitemap.xml (root pages), clean URLs where applicable.

---

## Performance and Quality

- **Budget:** <150KB CSS+JS gzipped on initial load; defer non‑critical scripts.
- **Assets:** Preload key fonts, use system fonts fallback, optimize and lazy‑load images/illustrations.
- **CSS/JS:** Minify for production; isolate critical CSS; avoid layout thrashing.
- **Motion:** Respects prefers‑reduced‑motion; no auto‑playing animations.

---

## Data Model and Coverage

- **Per‑grade JSON:** Each file groups topics into domains with fields for explanation, examples, generator configs, and solution keys.
- **Exercise schema:** id, topic, difficulty, prompt, data, steps, solution, hints, distractors (optional).
- **Localization:** Text nodes separated from logic; i18n keys later mapped to English.

---

## Running Locally

- **Static server:** Use any simple HTTP server to avoid CORS when fetching JSON.
- **Example (Python 3):**
  - **Command:** 
    ```
    python -m http.server 5173
    ```
  - **Access:** http://localhost:5173

---

## Roadmap

- **v0.1:** index.html shell, base styles, accessible components, placeholder data.
- **v0.2:** Routing and topic search; load Grade 1 JSON; exercise engine basics.
- **v1.0 (Italian):** Full Grades 1–5 JSON coverage; progress tracking; dark mode.
- **v1.1:** Print/export of practice sets; privacy‑friendly analytics (opt‑in).
- **v2.0 (English):** Full UI and content localization; parallel JSON datasets.

---

## Contributing

- **Issues:** Bug reports, enhancement requests, and topic coverage gaps are welcome.
- **Style:** Vanilla HTML/CSS/JS; keep accessibility, performance, and SEO intact.
- **Data:** Follow the JSON schema; validate before commits; add tests where possible.
- **Workflow:** Conventional commits and meaningful PR descriptions.

---

## License

- **MIT License:** Open, permissive use with attribution.

---

## Author

- **Name:** Bocaletto Luca
- **GitHub:** https://github.com/bocaletto-luca
- **Repository:** web-assistent
