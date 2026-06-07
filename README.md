# Hi, I'm Ryan Chen 👋

Software Engineer with a background in **Electrical Engineering & Computer Science**.  
Passionate about systems programming, network algorithms, and building practical web tools.

---

## 🛠️ Tech Stack

![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=c%2B%2B&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat&logo=tailwindcss&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)

---

## 🚀 Projects

| Project | Description | Tech | PC | Mobile |
|---|---|---|:---:|:---:|
| [SocratesApp](https://github.com/RyanChen0311/SocratesApp) | AI-powered Socratic learning system — generates a DAG skill tree of 12 knowledge nodes, scores responses via Claude API (0–20 pts), diagnoses misconceptions, and switches to teacher mode after 3 consecutive errors | C++, Drogon, PostgreSQL, D3.js | 🖥️ | — |
| [ip-lpm](https://github.com/RyanChen0311/ip-lpm) | IPv4 routing engine using Binary Trie for Longest Prefix Match — validated against real BGP data from RIPE NCC | C | — | — |
| [zhwiki-ir-mcqa](https://github.com/RyanChen0311/zhwiki-ir-mcqa) | Unsupervised Traditional Chinese multiple-choice QA system — builds inverted index over 1.2M Wikipedia articles, scores answer options via set intersection counting with jieba noun-only POS filtering, no ML or GPU required | Python | — | — |
| [path_elevator](https://github.com/RyanChen0311/path_elevator) | Filesystem path-traversal tool — displays every ancestor directory at once, like riding an elevator floor by floor | C++ | — | — |
| [calorie_survival](https://github.com/RyanChen0311/calorie_survival) | 7-day survival strategy game balancing calories, finances, exercise, and body weight across four daily phases — PWA with offline support, Zustand state persistence, and JSON-driven game balance config | React 18, TypeScript, Vite, Zustand, Tailwind CSS | 🖥️ | 📱 |
| [life-map](https://github.com/RyanChen0311/life-map) | Interactive graph visualizing 10 core life dimensions (career, health, habits, finance, etc.) with influence pathways, Canvas-rendered connections, and animated node glow effects | HTML5, CSS3, JavaScript | 🖥️ | — |
| [sleep-tracker](https://github.com/RyanChen0311/sleep-tracker) | Interactive sleep pattern visualizer with SVG timeline charts and deviation analysis between regular and actual sleep schedules | React, Vite, Tailwind CSS | 🖥️ | — |
| [parkour](https://github.com/RyanChen0311/parkour) | Browser-based parkour game with phantom ghost trail effects — four character classes, rainbow HSL color picker, speed control, and touch/keyboard controls; 23 Vitest unit tests with GitHub Actions CI | HTML5, CSS3, JavaScript | 🖥️ | 📱 |
| [vision-simulator](https://github.com/RyanChen0311/vision-simulator) | Real-time vision condition simulator covering myopia, hyperopia, astigmatism, and presbyopia with adjustable severity and Taiwan optical prescription standards | HTML5, CSS3, JavaScript | 🖥️ | 📱 |
| [pedometer](https://github.com/RyanChen0311/pedometer) | Mobile PWA step counter using DeviceMotion API with peak detection algorithm | JavaScript | — | 📱 |
| [nutrition-calculator](https://github.com/RyanChen0311/nutrition-calculator) | Calorie and macronutrient calculator using ACSM MET standards and a 24-hour energy metabolism model — dynamically adjusts protein intake by exercise duration and covers 11 vitamins and 10 minerals per DRI standards | JavaScript | 🖥️ | 📱 |
| [txt_scroll_div](https://github.com/RyanChen0311/txt_scroll_div) | TXT reader with smart paragraph/sentence-aware pagination | JavaScript | 🖥️ | — |
| [spell-english](https://github.com/RyanChen0311/spell-english) | Vocabulary flashcard app with Web Speech API pronunciation and localStorage | JavaScript | 🖥️ | 📱 |
| [discount_per](https://github.com/RyanChen0311/discount_per) | Bulk discount calculator with buyer and seller profit margin views | JavaScript | 🖥️ | 📱 |
| [nutrition-hunter](https://github.com/RyanChen0311/nutrition-hunter) | Daily nutrition tracker with hexagon radar chart (Canvas 2D), two-stage greedy food recommendation algorithm, Mifflin-St Jeor TDEE calculation, and a 33-item food database with localStorage persistence | JavaScript | 🖥️ | 📱 |

---

## ⭐ Featured Projects

**SocratesApp** — Socratic AI learning system built with C++ (Drogon) + Claude API + PostgreSQL.

I owned the full product design — learning flow, evaluation logic, and architectural decisions:

- **Skill graph**: Dynamic DAG of 9–12 nodes across 3 branches; each node requires 5 questions to ensure token-cost-predictable evaluation
- **Scoring**: Claude evaluates every response on a 0–20 continuous scale (not binary pass/fail), enabling partial-credit diagnosis; 60/100 passing threshold mirrors real academic credit standards
- **Teacher mode**: Triggered by **3 consecutive errors** (not cumulative) — consecutive failures isolate a genuine conceptual gap within the same causal chain, whereas cumulative counting conflates unrelated mistakes
- **Tech choice**: C++ chosen deliberately to build and demonstrate production-level systems programming skill alongside AI integration

AI was used as a development accelerator throughout — for code generation, iteration, and refinement — while all design decisions and their rationale remained mine.

**ip-lpm** — High-performance IPv4 routing engine implementing Longest Prefix Match via a 32-level Binary Trie, written in C and validated against real-world BGP data.

- **Why Binary Trie over Hash Table**: LPM requires finding the *longest* matching prefix — Hash Table can only do exact match, so it would need up to 33 separate lookups (one per prefix length /0–/32) per query. Binary Trie resolves this in a single O(32) traversal, naturally recording the deepest match along the way
- **Why C**: Manual `malloc`/`free` throughout — no RAII, no abstractions — to demonstrate low-level memory management and stay conceptually close to how real router FIB implementations work
- **Validation**: Tested against real BGP routing tables from RIPE NCC Route Collectors (Nov 2021), covering 800k–900k prefixes across 5 regions (rrc00/01/03/04/05) — self-generated test data cannot replicate real-world prefix distribution and edge cases

**zhwiki-ir-mcqa** — Unsupervised Traditional Chinese multiple-choice QA system built with Python, no ML or GPU required.

- **Scale**: Builds an inverted index over 1.2M Wikipedia articles — no preprocessing pipeline, runs entirely on local CPU
- **Answer scoring**: Set intersection counting between question context and each answer option; jieba POS filtering keeps nouns only, removing stop-word noise without a curated stoplist
- **Why noun-only**: Nouns carry the highest semantic density in Chinese; filtering shrinks per-article term sets and sharpens intersection signal without losing topical meaning
- **Why classical IR**: Demonstrates that a well-built inverted index over a large enough corpus can be competitive on structured QA without any model weights or fine-tuning

---

## 🧠 Engineering Highlights

Design decisions I made across AI-assisted projects — where I owned the system structure and engineering requirements, and used AI to implement them.

**calorie_survival**
- **Four-phase daily loop**: Designed morning / afternoon / evening / night as four distinct decision points, each with its own calorie, finance, and exercise trade-offs — the phase structure is the core game loop
- **JSON-driven balance config**: Required all numeric constants (calorie costs, weight-change rates, event weights) to live in a single config file rather than hardcoded — keeps tuning a data edit, not a code change
- **PWA + offline**: Specified service worker and manifest from the start so the game runs without a network connection and can be installed on a home screen

**parkour**
- **Testing requirement**: Specified 23 unit tests covering collision, scoring, and ghost trail logic, plus GitHub Actions CI on every push — deliberately held a browser game to the same engineering standard as production software
- **Four character classes**: Designed each class to alter speed, jump height, and trail color palette independently, so class choice has meaningful mechanical impact
- **Ghost trail concept**: Defined the phantom trail as a position-history replay at decreasing opacity — gave AI a clear behavioral spec to implement

---

## 📫 Contact

[![Email](https://img.shields.io/badge/Email-pig08082001@gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:pig08082001@gmail.com)
