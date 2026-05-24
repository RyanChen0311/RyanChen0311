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
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat&logo=tailwindcss&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)

---

## 🚀 Projects

| Project | Description | Tech |
|---|---|---|
| [SocratesApp](https://github.com/RyanChen0311/SocratesApp) | AI-powered Socratic learning system — generates a DAG skill tree of 12 knowledge nodes, scores responses via Claude API (0–20 pts), diagnoses misconceptions, and switches to teacher mode after 3 consecutive errors | C++, Drogon, PostgreSQL, D3.js |
| [ip-lookup-C](https://github.com/RyanChen0311/ip-lookup-C) | IPv4 routing engine using Binary Trie for Longest Prefix Match — validated against real BGP data from RIPE NCC | C |
| [QAbot](https://github.com/RyanChen0311/QAbot) | Unsupervised Traditional Chinese QA system using Wikipedia-scale inverted index + jieba POS tagging | Python |
| [Elevator-Simulator](https://github.com/RyanChen0311/Elevator-Simulator) | Multi-elevator dispatch system implementing the nearest-car algorithm | C++ |
| [life-map](https://github.com/RyanChen0311/life-map) | Interactive graph visualizing 10 core life dimensions (career, health, habits, finance, etc.) with influence pathways, Canvas-rendered connections, and animated node glow effects | HTML5, CSS3, JavaScript |
| [sleep-analysis-chart](https://github.com/RyanChen0311/sleep-analysis-chart) | Interactive sleep pattern visualizer with SVG timeline charts and deviation analysis between regular and actual sleep schedules | React, Vite, Tailwind CSS |
| [parkour](https://github.com/RyanChen0311/parkour) | Browser-based parkour game with phantom ghost trail effects — four character classes (Archer, Mage, Swordsman, Assassin), touch/keyboard controls, and auto mode | HTML5, CSS3, JavaScript |
| [vision_status_processor](https://github.com/RyanChen0311/vision_status_processor) | Real-time vision condition simulator covering myopia, hyperopia, astigmatism, and presbyopia with adjustable severity and Taiwan optical prescription standards | HTML5, CSS3, JavaScript |
| [pedometer](https://github.com/RyanChen0311/pedometer) | Mobile PWA step counter using DeviceMotion API with peak detection algorithm | JavaScript |
| [skill-of-hunter](https://github.com/RyanChen0311/skill-of-hunter) | Interactive Nen ability radar chart with Canvas API and polar coordinate drag | JavaScript |
| [txt_scroll_div](https://github.com/RyanChen0311/txt_scroll_div) | TXT reader with smart paragraph/sentence-aware pagination | JavaScript |
| [learn_english_for_resite](https://github.com/RyanChen0311/learn_english_for_resite) | Vocabulary flashcard app with Web Speech API pronunciation and localStorage | JavaScript |
| [languages-translator_5ls](https://github.com/RyanChen0311/languages-translator_5ls) | 5-language translator using Google Translate API with keyboard navigation | JavaScript |
| [discount_per](https://github.com/RyanChen0311/discount_per) | Bulk discount calculator with buyer and seller profit margin views | JavaScript |
| [money-eye-bubble-tea](https://github.com/RyanChen0311/money-eye-bubble-tea) | Live USD→TWD exchange rate calculator for bubble tea purchasing | JavaScript |

---

## ⭐ Featured Project — SocratesApp

**Socratic AI learning system** built with C++ (Drogon) + Claude API + PostgreSQL.

I owned the full product design — learning flow, evaluation logic, and architectural decisions:

- **Skill graph**: Dynamic DAG of 9–12 nodes across 3 branches; each node requires 5 questions to ensure token-cost-predictable evaluation
- **Scoring**: Claude evaluates every response on a 0–20 continuous scale (not binary pass/fail), enabling partial-credit diagnosis; 60/100 passing threshold mirrors real academic credit standards
- **Teacher mode**: Triggered by **3 consecutive errors** (not cumulative) — consecutive failures isolate a genuine conceptual gap within the same causal chain, whereas cumulative counting conflates unrelated mistakes
- **Tech choice**: C++ chosen deliberately to build and demonstrate production-level systems programming skill alongside AI integration

AI was used as a development accelerator throughout — for code generation, iteration, and refinement — while all design decisions and their rationale remained mine.

---

## 📫 Contact

[![Email](https://img.shields.io/badge/Email-pig08082001@gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:pig08082001@gmail.com)
