# Contributing to PhishShield 🛡️

Thank you for your interest in improving PhishShield! This guide explains how to contribute effectively.

---

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How to Contribute](#how-to-contribute)
- [Development Setup](#development-setup)
- [Project Structure](#project-structure)
- [Contribution Ideas](#contribution-ideas)
- [Pull Request Process](#pull-request-process)

---

## Code of Conduct

This project is for **educational and defensive cybersecurity purposes only**. Contributors must agree that:

- No contributions may enable, facilitate, or assist real phishing attacks
- All scenarios and examples must be clearly fictional
- Respectful, inclusive communication is expected at all times

---

## How to Contribute

### 🐛 Reporting Bugs

1. Check [existing issues](https://github.com/your-username/phishshield/issues) first
2. Open a new issue with:
   - Clear title describing the bug
   - Steps to reproduce
   - Expected vs actual behavior
   - Browser and OS details

### 💡 Suggesting Features

Open an issue with the label `enhancement` and describe:
- What problem it solves
- How it would work
- Any design considerations

### 🔧 Submitting Code

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Make your changes to `index.html`
4. Test in multiple browsers (Chrome, Firefox, Safari)
5. Open a Pull Request with a clear description

---

## Development Setup

```bash
# Clone your fork
git clone https://github.com/YOUR-USERNAME/phishshield.git
cd phishshield

# No build step needed! Just open in browser
open index.html

# Or use a local server for better dev experience
python -m http.server 8080
# Visit http://localhost:8080
```

---

## Project Structure

Since PhishShield is a single-file app, all changes go into `index.html`:

```
index.html
├── <head>          → Fonts, meta tags
├── <style>         → All CSS (CSS custom properties, layout, components)
├── <body>          → All HTML pages (nav, page divs, modals)
└── <script>        → All JavaScript (DB, auth, quiz, games, AI, utils)
```

### Key JavaScript Sections (in order)
| Section | What it does |
|---------|-------------|
| `DB` object | localStorage user/session/leaderboard management |
| `secTitle()` | Maps quiz score → title + color |
| `setTheme()` | Dark/light/system theme toggle |
| `go()` | SPA page navigation |
| `doAuth()` | Login/signup logic |
| `SCENARIOS[]` | Quiz email data |
| Quiz Engine | `startQuiz`, `renderQ`, `answerQ`, `showResults` |
| `ATTACKS[]` | Encyclopedia attack data |
| `renderEncyclopedia()` | Renders accordion from ATTACKS data |
| Games Data | `POL_EMAILS`, `URL_ROUNDS`, `ATQ_ROUNDS`, `SE_SCENARIOS` |
| Game Engines | `initPOL/URL/ATQ/SE`, `render*`, `answer*`, `end*` |
| `runSim()` | Role-based AI simulator (no API key) |
| `pgGenerateScenario()` | Custom simulator (requires API key) |
| `doReport()` | Report-a-phish AI analysis |

---

## Contribution Ideas

### 🟢 Good First Issues
- Add more quiz scenarios to `SCENARIOS[]`
- Add more URL pairs to `URL_ROUNDS[]`
- Add more Social Engineering scenarios to `SE_SCENARIOS[]`
- Fix typos or improve descriptions in `ATTACKS[]`
- Improve mobile responsiveness

### 🟡 Intermediate
- Add a new mini-game
- Add a "Password Strength Checker" tool page
- Add progress persistence across sessions
- Add share-score functionality (copy to clipboard)

### 🔴 Advanced
- PWA support (service worker + manifest)
- i18n / multilingual support
- Export training completion certificate (PDF)
- Organization/team mode with shared leaderboards

---

## Adding Quiz Scenarios

Add to the `SCENARIOS` array in `index.html`:

```javascript
{
  id: 6,                           // Unique ID
  diff: 'hard',                    // 'easy' | 'medium' | 'hard'
  cat: 'Category Name',            // Shown as tag
  subj: 'Email Subject Line',
  sender: {
    d: 'Display Name <display@domain.com>',   // What user sees
    a: 'actual@attacker-domain.xyz'           // Real sender (X-Ray)
  },
  body: `Email body text here.
  
  Click here: http://fake-link.com/path`,
  links: [
    { d: 'http://fake-link.com/path', a: 'http://real-malicious-destination.ru' }
  ],
  rf: [                            // Red flags (shown after answer)
    { t: 'Description of red flag', k: 'DOMAIN' }  // k: DOMAIN|URGENCY|SENSITIVE|THREAT|MANIPULATION
  ],
  fish: true,                      // true = phishing, false = legitimate
  explain: 'Explanation shown after user answers.'
}
```

---

## Pull Request Process

1. Ensure your changes work in Chrome, Firefox, and Safari
2. Keep the single-file structure — no new files unless absolutely necessary
3. Write a clear PR description explaining what changed and why
4. Link any related issues with `Closes #123`
5. A maintainer will review within a few days

---

## Questions?

Open a [GitHub Discussion](https://github.com/your-username/phishshield/discussions) or an issue tagged `question`.

---

*Happy contributing — and stay phish-free! 🎣🚫*
