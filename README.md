# 🛡️ PhishShield — Advanced Phishing Awareness Platform

> *"The False Bottom" — Learn to spot deception hiding beneath every email, call, and link.*

![PhishShield Banner](https://img.shields.io/badge/PhishShield-v2.0-00c8ff?style=for-the-badge&logo=shield&logoColor=white)
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Claude AI](https://img.shields.io/badge/Claude_AI-Powered-bf7fff?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

---

## 🔴 Live Demo

> **[▶ Launch PhishShield](https://your-username.github.io/phishshield)**

---

## 📸 Screenshots

| Home | Quiz | Games | Encyclopedia |
|------|------|-------|--------------|
| ![Home](docs/screenshots/home.png) | ![Quiz](docs/screenshots/quiz.png) | ![Games](docs/screenshots/games.png) | ![Encyclopedia](docs/screenshots/encyclopedia.png) |

---

## 🎯 What is PhishShield?

PhishShield is a **fully interactive, AI-powered cybersecurity awareness training platform** built as a single-file web app. It teaches users to recognize and defend against modern phishing attacks through hands-on simulations, real-world quiz scenarios, and gamified learning.

No installation. No backend. No database. Just open `index.html` and start training.

---

## ✨ Features

### 🎯 Detection Challenge (Quiz)
- 5 real-world phishing email scenarios
- **X-Ray Mode** — hover over sender addresses and links to reveal hidden destinations
- Detailed AI-powered explanation after each answer
- Score saved to your profile and global leaderboard

### 🎮 4 Security Mini-Games
| Game | Description | Max Points |
|------|-------------|-----------|
| 🃏 **Phish or Legit?** | 10 rapid-fire emails — judge each against the clock | 200 pts |
| 🔗 **URL Detective** | Spot the fake URL from look-alike pairs | 160 pts |
| 🧩 **Attack Type Quiz** | Identify the attack category from a scenario | 120 pts |
| 🕵️ **Social Eng. Survival** | Navigate real social engineering scenarios | 150 pts |

### 📖 Attack Encyclopedia
Deep-dive into **8 attack vectors** with visual mock-UIs, real-world examples, and red flags:

| Attack | Type | Risk |
|--------|------|------|
| 📞 Vishing | Voice Phishing | 🔴 HIGH |
| 💬 Smishing | SMS Phishing | 🔴 HIGH |
| 🌐 Pharming | DNS Hijacking | 🔴 HIGH |
| 📷 Quishing | QR Code Phishing | 🟡 MED |
| 📧 Clone Phishing | Email Cloning | 🔴 HIGH |
| 📶 Evil Twin | Rogue Wi-Fi | 🔴 HIGH |
| 🐦 Angler Phishing | Social Media | 🟡 MED |
| 🤖 Deepfake Phishing | AI Voice/Video | 🔴 HIGH |

### 🤖 AI Phishing Simulator
- Role-based simulator: Finance, HR, C-Suite, IT Admin, Healthcare, and more
- Generates realistic phishing emails using **Claude AI**
- X-Ray sender inspection built in
- Optional: Custom scenarios with your own Anthropic API key

### 🚩 Report-a-Phish Hub
- Paste any suspicious email and get instant AI threat analysis
- Returns: verdict, confidence %, red flags, safe indicators, and recommendation

### 👤 User System & Leaderboard
- Sign up / Sign in (localStorage-based, no backend needed)
- Personal dashboard: Security IQ, global rank, title, game points
- Global leaderboard with seeded competitors

### 🌙 Dark / Light / System Theme
- Full dark and light mode with smooth transitions
- System preference detection

---

## 🚀 Getting Started

### Option 1 — Open directly (simplest)
```bash
# Clone the repo
git clone https://github.com/your-username/phishshield.git

# Open in your browser
open phishshield/index.html
```

### Option 2 — GitHub Pages (recommended for sharing)
1. Fork this repository
2. Go to **Settings → Pages**
3. Set source to **main branch / root**
4. Your site will be live at `https://your-username.github.io/phishshield`

### Option 3 — Local server
```bash
# Using Python
cd phishshield
python -m http.server 8080
# Visit http://localhost:8080

# Using Node.js
npx serve .
```

---

## 🤖 AI Features Setup

PhishShield includes two AI-powered features:

### Role-Based Simulator (No setup required)
Works out of the box — uses the Anthropic API with browser-side CORS headers.

### Custom Scenario Simulator + Report-a-Phish
These features require an **Anthropic API key**:
1. Get your key at [console.anthropic.com](https://console.anthropic.com)
2. In the app, navigate to **AI Sim → Custom Scenario**
3. Paste your key (format: `sk-ant-api03-...`)

> ⚠️ Your API key is **never stored** — it only lives in your browser session.

---

## 🗂️ Project Structure

```
phishshield/
│
├── index.html          # Complete single-file application (HTML + CSS + JS)
├── README.md           # This file
├── LICENSE             # MIT License
├── CONTRIBUTING.md     # How to contribute
├── .gitignore          # Git ignore rules
│
└── docs/
    ├── screenshots/    # App screenshots for README
    └── SECURITY.md     # Security policy & responsible disclosure
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Structure | HTML5 |
| Styling | CSS3 (Custom Properties, Grid, Flexbox, Animations) |
| Logic | Vanilla JavaScript (ES6+) |
| AI | Anthropic Claude API (`claude-sonnet-4-6`) |
| Storage | localStorage (client-side only) |
| Fonts | Google Fonts (Orbitron, Space Mono, Syne, IBM Plex Mono) |
| Hosting | GitHub Pages |

**Zero dependencies. Zero build tools. Zero backend.**

---

## 📊 Why PhishShield?

| Stat | Value |
|------|-------|
| Phishing emails sent daily | **3.4 Billion** |
| Cyberattacks starting with phishing | **91%** |
| Average breach cost (2024) | **$4.9 Million** |
| Time to click a phishing link | **17 seconds** |

Traditional security training is boring. PhishShield makes it interactive, gamified, and actually memorable.

---

## 🔒 Privacy & Security

- **No data leaves your device** — all user data stored in `localStorage`
- **No analytics, no tracking, no ads**
- API keys are session-only and never persisted
- Designed for educational use only — no real phishing infrastructure

---

## 🤝 Contributing

Contributions are welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

Ideas for contributions:
- [ ] More quiz scenarios
- [ ] Additional game modes
- [ ] Multilingual support (i18n)
- [ ] Mobile PWA support
- [ ] Export training certificate as PDF
- [ ] Team/organization mode

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

Free to use, modify, and distribute for educational purposes.

---

## ⚠️ Disclaimer

PhishShield is built **exclusively for security awareness training and education**. All phishing examples are simulated and fictional. Do not use this tool or its content for any malicious purpose.

---

<div align="center">
  <strong>🛡️ PhishShield // THE FALSE BOTTOM</strong><br>
  <em>AI-Powered Cybersecurity Education · Built with ❤️ for a safer internet</em>
</div>
