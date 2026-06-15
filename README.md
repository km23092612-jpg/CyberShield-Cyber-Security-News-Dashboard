# 🛡️ CyberShield — Cyber Security News Dashboard

> **Capstone Project 4 of 4** — Cybrexa Technologies Learning Track  
> `HTML` • `CSS` • `JavaScript` • `Chart.js` • `No frameworks required`

![CyberShield Preview](https://img.shields.io/badge/Status-Live-00ffb4?style=for-the-badge&logo=shield&logoColor=black)
![Tech Stack](https://img.shields.io/badge/Stack-HTML%20%7C%20CSS%20%7C%20JS-00c8ff?style=for-the-badge)
![Level](https://img.shields.io/badge/Level-Intermediate-ff8c42?style=for-the-badge)

---

## 🎯 Project Overview

CyberShield is a **professional-grade, single-page cybersecurity intelligence dashboard** that aggregates real-time threat news, visualizes attack analytics, streams live security events, performs IP intelligence lookups, and provides an interactive security knowledge hub.

Built as a fully self-contained HTML/CSS/JavaScript application — no build tools, no backend required.

---

## ✨ Features

### 1. 📰 News Aggregator
- Simulated real-time cybersecurity news feed with severity tagging (Critical / High / Medium / Low)
- Full-text search across titles, descriptions, and CVE IDs
- Filter buttons: All · Critical · High · Medium · Malware · CVE
- Live CVE list with CVSS score display
- Animated threat category bar chart
- Auto-refresh indicator every 3 seconds

### 2. 📊 Threat Analytics
- **CVSS Severity Distribution** — Bar chart (Chart.js) across Critical / High / Medium / Low
- **Attack Vectors** — Doughnut chart showing Network, Social Engineering, Supply Chain, Physical
- **30-Day Threat Timeline** — Multi-series line chart with threat vs patch trend
- **Top Targeted Sectors** — Animated bar chart (Healthcare, Finance, Government, etc.)
- **Active CVE Tracker** — Full sortable table with CVSS scores, affected software, and status badges

### 3. ⚡ Live Monitor
- **Real-time event log** that auto-injects simulated security events every 1.2 seconds
- Pause / Resume and Clear controls
- Color-coded log types: `[CRIT]` `[WARN]` `[INFO]` `[OK]`
- **Live network traffic chart** — Inbound vs Blocked, auto-updating every 3s
- **System health panel** — 6 security services with live status indicators
- **Geolocation attack map** — SVG world map with animated ripple dots per attack origin
- Top attack source countries with proportional volume bars

### 4. 🔍 IP & Source Intelligence
- IP/domain lookup with simulated threat scoring (0–100 risk score)
- Returns: Country, ISP, Organization, IP Type, Open Ports, Last Seen, ASN, Blacklist status
- Threat level pill with color-coded risk (LOW → CRITICAL)
- Recent lookup history panel with one-click re-scan
- Blacklist database status (Spamhaus, AbuseIPDB, EmergingThreats, Feodo Tracker, etc.)
- IP reputation trend line chart (30-day risk evolution)

### 5. 📚 Knowledge Hub
- **Security Glossary** — 12+ key terms with definitions, categories, and severity tags
- Full-text glossary search
- **Security Frameworks grid** — MITRE ATT&CK, NIST CSF 2.0, OWASP Top 10, ISO 27001, CIS Controls v8, Zero Trust
- **Learning Resources** — CISA Training, OWASP Docs, TryHackMe, MITRE ATT&CK links

---

## 🚀 Getting Started

### Option A — Open directly (no setup needed)
```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/Cybrexa_04_CyberShield.git
cd Cybrexa_04_CyberShield

# Open in browser
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

### Option B — Serve locally (recommended for full feature testing)
```bash
# Using Python (built-in)
python3 -m http.server 8080
# Visit http://localhost:8080

# Using Node.js
npx serve .
# Visit http://localhost:3000

# Using VS Code
# Install "Live Server" extension → right-click index.html → "Open with Live Server"
```

---

## 📁 Project Structure

```
Cybrexa_04_CyberShield/
│
├── index.html          # Complete single-file application
├── README.md           # This file
└── assets/             # (optional) screenshots for documentation
    └── preview.png
```

> **Why single-file?** This project is intentionally self-contained — all CSS and JavaScript is embedded in `index.html` for maximum portability and simplicity of deployment.

---

## 🌐 Deployment

### GitHub Pages (Free hosting)
```bash
# 1. Push to GitHub
git init
git add .
git commit -m "feat: initial CyberShield dashboard"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/Cybrexa_04_CyberShield.git
git push -u origin main

# 2. Go to repo Settings → Pages
# 3. Set Source: Deploy from branch → main → / (root)
# 4. Your live URL: https://YOUR_USERNAME.github.io/Cybrexa_04_CyberShield/
```

### Netlify (Drag & Drop)
1. Go to [netlify.com](https://netlify.com) → "Add new site" → "Deploy manually"
2. Drag your project folder into the upload area
3. ✅ Live in 30 seconds

### Vercel
```bash
npx vercel --prod
```

---

## 🛠️ Tech Stack

| Technology | Usage |
|---|---|
| HTML5 | Semantic structure, single-page layout |
| CSS3 | Custom properties, grid, animations, dark theme |
| Vanilla JavaScript | DOM manipulation, state management, data rendering |
| Chart.js 4.4.1 | Bar, line, doughnut, and area charts |
| Google Fonts (Inter + JetBrains Mono) | Typography system |
| SVG | World map visualization, shield logo |

**Zero dependencies** beyond Chart.js and Google Fonts (both CDN-loaded).

---

## 🎨 Design System

| Token | Value |
|---|---|
| Primary Background | `#0a0e1a` |
| Card Surface | `#111827` |
| Accent (Terminal Green) | `#00ffb4` |
| Accent (Cyber Blue) | `#00c8ff` |
| Critical Red | `#ff4d4d` |
| Warning Orange | `#ff8c42` |
| Display Font | JetBrains Mono |
| Body Font | Inter |

---

## 📋 Deliverables Checklist

- [x] `index.html` — Complete, self-contained dashboard
- [x] Live deploy via GitHub Pages / Netlify
- [x] README.md with setup, architecture, and deployment steps
- [x] All 5 required modules implemented
- [x] Auto-refresh at 3-second intervals on Live Monitor
- [x] Responsive layout (mobile-friendly grid)
- [x] Chart.js visual analytics
- [x] IP intelligence lookup module
- [x] Cybersecurity knowledge hub with glossary

---

## 📸 Screenshots

> Add screenshots of each panel to `assets/` and reference them here after deployment.

| Panel | Preview |
|---|---|
| News Feed | `assets/news.png` |
| Threat Analytics | `assets/analytics.png` |
| Live Monitor | `assets/monitor.png` |
| IP Intelligence | `assets/ip.png` |
| Knowledge Hub | `assets/knowledge.png` |

---

## 🔧 Customization

### Add Real News Data
Replace `newsData` array in the `<script>` section with a real API fetch:
```javascript
// Example: NewsAPI.org (requires free API key)
const res = await fetch(`https://newsapi.org/v2/everything?q=cybersecurity&apiKey=YOUR_KEY`);
const { articles } = await res.json();
```

### Add Real IP Lookup
Replace `lookupIP()` mock with:
```javascript
// AbuseIPDB API (free tier: 1000 checks/day)
const res = await fetch(`https://api.abuseipdb.com/api/v2/check?ipAddress=${ip}`, {
  headers: { 'Key': 'YOUR_API_KEY', 'Accept': 'application/json' }
});
```

---

## 👨‍💻 Author

**Your Name**  
GitHub: [@YOUR_USERNAME](https://github.com/YOUR_USERNAME)  
Cybrexa Cohort 2025 — Capstone Project 4

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

*Built with ❤️ and ☕ for the Cybrexa Capstone Program*
