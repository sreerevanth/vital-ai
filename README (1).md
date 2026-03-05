<div align="center">

<img src="https://img.shields.io/badge/VitalAI-Health%20Intelligence-0284C7?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0xMiAyQzYuNDggMiAyIDYuNDggMiAxMnM0LjQ4IDEwIDEwIDEwIDEwLTQuNDggMTAtMTBTMTcuNTIgMiAxMiAyek0xMyAxN2gtMnYtNkg5bDMtM2wzIDN6Ii8+PC9zdmc+" alt="VitalAI">

# 🩺 VitalAI

### Personal Health Intelligence — Powered by Groq AI

**Upload any blood report. Get a plain-language doctor-style assessment in seconds.**  
Built for Indian families. Free forever. No subscriptions, no data collection.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Open%20App-0EA5E9?style=flat-square)](https://your-username.github.io/vitalai)
[![License](https://img.shields.io/badge/License-MIT-22C55E?style=flat-square)](LICENSE)
[![Groq Powered](https://img.shields.io/badge/AI-Groq%20llama--3.3--70b-A855F7?style=flat-square)](https://groq.com)
[![No Backend](https://img.shields.io/badge/Backend-None%20Required-F59E0B?style=flat-square)](#)
[![Made in India](https://img.shields.io/badge/Made%20in-India%20🇮🇳-FF9933?style=flat-square)](#)

<br>

![VitalAI Screenshot](https://via.placeholder.com/900x500/0EA5E9/FFFFFF?text=VitalAI+Screenshot+%E2%80%94+Replace+with+actual+screenshot)

</div>

---

## ✨ What is VitalAI?

Most Indians get blood tests done regularly — but understanding what the results actually *mean* requires either a ₹800 doctor's appointment or googling each value separately. VitalAI fixes that.

Drop in your blood report from **SRL, Dr Lal PathLabs, Thyrocare**, or any other lab — and get back a full, doctor-style assessment: what's normal, what's concerning, why it matters, and what to do next. All in plain language. In under 10 seconds.

It also works as a **symptom checker** — describe what you're feeling and get clear triage guidance for yourself or any family member.

---

## 🎯 Features

| Feature | Description |
|---------|-------------|
| 🩸 **PDF Blood Report Analysis** | Upload any lab PDF — text is extracted directly in the browser using PDF.js |
| ✍️ **Manual Value Entry** | Enter 12 common markers manually if you don't have a PDF |
| 🏥 **Full AI Assessment** | Verdict, health score (0–100), per-marker breakdown with range bars |
| ⚠️ **Issues & Recommendations** | Colour-coded alerts (critical / warning / info) with specific action items |
| 💬 **Symptom Checker** | Conversational AI doctor — describe symptoms, get triage guidance |
| 👨‍👩‍👧‍👦 **Family Profiles** | Track health for multiple family members in one place |
| 📊 **Trend Comparison** | Compare results over time — see what's improving |
| 🖨️ **Print & Share** | Print-optimised report layout, copy summary to clipboard |
| 🔒 **100% Private** | Your API key and medical data stay in your browser — nothing is stored or sent to our servers |

---

## 🚀 Quick Start

VitalAI is a **single HTML file**. No installation, no backend, no server.

### Option 1 — Open directly in browser
```bash
# Download the file
curl -O https://raw.githubusercontent.com/your-username/vitalai/main/VitalAI.html

# Open in your browser
open VitalAI.html        # macOS
start VitalAI.html       # Windows
xdg-open VitalAI.html   # Linux
```

### Option 2 — Clone and run
```bash
git clone https://github.com/your-username/vitalai.git
cd vitalai
open VitalAI.html
```

### Option 3 — GitHub Pages (recommended for sharing)
1. Fork this repository
2. Go to **Settings → Pages**
3. Set source to **main branch / root**
4. Your app is live at `https://your-username.github.io/vitalai`

---

## 🔑 Getting Your Free Groq API Key

VitalAI uses **Groq's free API** to power the AI analysis. No credit card required.

1. Go to [console.groq.com](https://console.groq.com)
2. Sign up (takes 60 seconds)
3. Navigate to **API Keys → Create API Key**
4. Copy the key — it starts with `gsk_`
5. Paste it into VitalAI when prompted

> **Free tier limits:** 14,400 requests/day — more than enough for personal and family use.

---

## 🧠 How It Works

```
User uploads PDF / enters values
         ↓
PDF.js extracts text in the browser (no server needed)
         ↓
Full report text sent to Groq API (llama-3.3-70b-versatile)
         ↓
AI returns structured JSON: markers, issues, recommendations
         ↓
VitalAI renders colour-coded cards, score ring, action items
```

**The AI model used:** `llama-3.3-70b-versatile` via Groq  
**Why Groq?** It's the fastest inference API available, completely free for personal use, and requires no credit card.

---

## 📊 Blood Markers Supported

| Category | Markers |
|----------|---------|
| **Haematology** | Hemoglobin, WBC, Platelets, RBC, MCV, MCH, MCHC |
| **Metabolic** | Fasting Glucose, HbA1c, Creatinine, BUN, Uric Acid |
| **Liver** | SGOT/AST, SGPT/ALT, ALP, Bilirubin, Albumin |
| **Lipid Profile** | Total Cholesterol, HDL, LDL, VLDL, Triglycerides |
| **Thyroid** | TSH, Free T3, Free T4 |
| **Nutritional** | Vitamin D, Vitamin B12, Serum Iron, Ferritin |
| **Electrolytes** | Sodium, Potassium, Calcium |

> When uploading a PDF, **all markers in the report are extracted and analyzed** — not just the ones listed above.

---

## 🗂️ Project Structure

```
vitalai/
├── VitalAI.html              # The entire app — single file
├── BloodReport_Rahul_Sharma.pdf  # Sample test report for demo
├── README.md                 # This file
└── LICENSE                   # MIT License
```

That's it. One file. No `node_modules`, no build step, no config.

---

## 🔒 Privacy & Security

- **Your API key** is stored only in browser memory — never written to localStorage, never sent to anyone except Groq's servers
- **Your medical data** is sent directly from your browser to Groq's API — VitalAI has no server that touches your data
- **Nothing is persisted** between sessions — closing the tab clears everything
- **Open source** — you can read every line of code in `VitalAI.html`

> VitalAI is designed with a **privacy-first** architecture specifically because medical data is sensitive.

---

## ⚠️ Medical Disclaimer

VitalAI is an **educational tool**, not a medical device. It is not a substitute for professional medical advice, diagnosis, or treatment.

- Results should be discussed with a qualified doctor
- Do not make medical decisions based solely on VitalAI's output
- In an emergency, call **112** immediately

---

## 🛣️ Roadmap

- [ ] Hindi & regional language support
- [ ] Mobile app (React Native)
- [ ] Fine-tuned model on Indian lab formats (SRL, Dr Lal, Thyrocare)
- [ ] WhatsApp bot integration
- [ ] Offline mode via Ollama (local AI, zero cloud)
- [ ] Clinic API — white-label for diagnostic labs
- [ ] Wearables integration (smartwatch vitals)

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

```bash
# Fork the repo on GitHub, then:
git clone https://github.com/your-username/vitalai.git
cd vitalai

# Make your changes to VitalAI.html
# Test by opening the file in your browser

# Submit a pull request
```

**Ideas for contributions:**
- Support for more blood markers
- Better parsing for specific lab report formats
- UI improvements
- Translations (Hindi, Tamil, Telugu, etc.)
- Testing with different lab report PDFs

---

## 🧪 Testing with the Sample Report

A realistic sample blood report is included (`BloodReport_Rahul_Sharma.pdf`) — a 38-year-old male with 6 deliberate health issues for testing:

| Finding | Severity |
|---------|----------|
| Iron Deficiency Anaemia (Hgb 9.4) | 🚨 Critical |
| Pre-Diabetes (HbA1c 6.2%) | ⚠️ Warning |
| Dyslipidaemia (High LDL, Low HDL) | ⚠️ Warning |
| Subclinical Hypothyroidism (TSH 5.8) | ⚠️ Warning |
| Severe Vitamin D Deficiency (14.2) | ⚠️ Warning |
| Elevated Liver Enzymes (SGPT 55) | ℹ️ Info |

Upload this PDF to verify the AI catches all 6 issues.

---

## 📄 License

MIT License — free to use, modify, and distribute. See [LICENSE](LICENSE) for details.

---

<div align="center">

Built with ❤️ for Indian families

**[⭐ Star this repo](https://github.com/your-username/vitalai)** if VitalAI helped you understand your health better.

*VitalAI is not affiliated with SRL Diagnostics, Dr Lal PathLabs, Thyrocare, or Groq.*

</div>
