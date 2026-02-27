# 🤖 Friday — Personal AI Assistant

<div align="center">

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![No Framework](https://img.shields.io/badge/No_Framework-Pure_JS-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-purple?style=for-the-badge)

<br/>

> **Friday is a lightweight, voice-enabled personal AI assistant built with pure HTML, CSS, and JavaScript — inspired by JARVIS. Built by Sandesh.**

<br/>

[🚀 Live Demo](#-live-demo) • [✨ Features](#-features) • [⚙️ Installation](#️-installation) • [🗺️ Roadmap](#️-roadmap)

</div>

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Live Demo](#-live-demo)
- [Features](#-features)
- [How It Works](#-how-it-works)
- [Installation](#️-installation)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [Customization](#-customization)
- [Roadmap](#️-roadmap)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## 🧠 Overview

**Friday** is a browser-based personal AI assistant that listens to your questions and responds with both **text and voice**. Built entirely with vanilla HTML, CSS, and JavaScript — no frameworks, no backend, no installation required.

Just open the file in a browser and start talking to your assistant. 🎤

The name is inspired by Tony Stark's AI assistant **F.R.I.D.A.Y.** from the Marvel universe — and just like the movie version, this Friday is always ready to help.

---

## 🌐 Live Demo

> Open `index.html` directly in any modern browser — no server required!

```bash
# Just double-click index.html OR run with Live Server in VS Code
```

---

## ✨ Features

| Feature | Description |
|---|---|
| 🎤 **Voice Replies** | Friday speaks her responses using the Web Speech API |
| 💬 **Text Responses** | Clean, readable text output in the chat window |
| 🕐 **Real-Time Clock** | Ask "what's the time?" and get the current time instantly |
| 📅 **Date Awareness** | Ask "what's the date?" for today's date |
| 🙋 **Identity Aware** | Knows her name and who created her |
| 🎨 **Beautiful UI** | Dark gradient background with glassmorphism card design |
| ⚡ **Zero Dependencies** | Pure HTML + CSS + JS, no libraries or frameworks needed |
| 📱 **Responsive Design** | Works on desktop and mobile browsers |

---

## ⚙️ How It Works

```
User types a question
        │
        ▼
getResponse() is triggered
        │
        ▼
generateResponse() matches keywords
  ├── "your name"   → Returns Friday's name
  ├── "who made you" → Credits Sandesh
  ├── "hello / hi"  → Greeting response
  ├── "time"        → Returns current time
  ├── "date"        → Returns today's date
  └── (anything else) → Default fallback reply
        │
        ▼
Response shown in the chat window
        │
        ▼
Web Speech API (SpeechSynthesisUtterance) speaks the reply aloud 🔊
```

---

## 🛠️ Installation

No installation needed! This is a pure front-end project.

### Option 1 — Direct Open
```bash
# Download or clone the repository
git clone https://github.com/YOUR_USERNAME/friday-ai-assistant.git

# Open index.html in your browser
open index.html        # Mac
start index.html       # Windows
xdg-open index.html    # Linux
```

### Option 2 — VS Code Live Server
1. Install the **Live Server** extension in VS Code
2. Right-click `index.html`
3. Select **"Open with Live Server"**
4. Friday opens at `http://127.0.0.1:5500`

### Option 3 — Deploy to GitHub Pages
1. Push the project to a GitHub repository
2. Go to **Settings → Pages**
3. Set source to `main` branch → `/root`
4. Your assistant will be live at `https://YOUR_USERNAME.github.io/friday-ai-assistant`

---

## 🚀 Usage

1. Open `index.html` in your browser
2. Type your question in the input box
3. Click the **Ask** button (or press Enter)
4. Friday replies in text AND speaks the answer aloud 🎤

### Example Questions You Can Ask

| You Say | Friday Replies |
|---|---|
| `Hello` | "Hello! How can I assist you today?" |
| `What is your name?` | "My name is Friday, your AI assistant created by Sandesh." |
| `Who made you?` | "I was proudly created by Sir Sandesh." |
| `What time is it?` | "The current time is 10:45:32 AM" |
| `What is today's date?` | "Today's date is 6/15/2024" |

---

## 🗂️ Project Structure

```
friday-ai-assistant/
│
├── index.html        # Main application file (UI + Logic)
├── style.css         # External stylesheet (optional overrides)
└── README.md         # Project documentation
```

> All core logic, styles, and structure live in `index.html` for simplicity.

---

## 🎨 Customization

### Change the Assistant's Name
In `index.html`, find and update:
```html
<h1>👋 Hello, I'm <span class="name">Friday</span></h1>
```

### Change the Creator's Name
```html
<p>...built by <strong>Sandesh</strong>...</p>
```
And in the JavaScript:
```javascript
if (lower.includes('who made you')) return "I was proudly created by Sir Sandesh.";
```

### Change the Background Color
```css
background: linear-gradient(to right, #04020f, #a297d1);
```
Replace the hex values with your preferred colors.

### Add New Responses
In the `generateResponse()` function, add a new `if` block:
```javascript
if (lower.includes('weather')) return "I can't check live weather yet, but it's always sunny when I'm around! ☀️";
if (lower.includes('joke')) return "Why do programmers prefer dark mode? Because light attracts bugs! 🐛";
```

### Change the Voice
```javascript
const utterThis = new SpeechSynthesisUtterance(reply);
utterThis.voice = synth.getVoices()[0]; // Change index to try different voices
utterThis.rate = 1.0;   // Speed: 0.1 to 10
utterThis.pitch = 1.0;  // Pitch: 0 to 2
synth.speak(utterThis);
```

---

## 🛣️ Roadmap

- [x] Basic keyword-based responses
- [x] Text-to-speech voice replies
- [x] Real-time time and date
- [x] Glassmorphism dark UI
- [ ] Speech-to-text (voice input)
- [ ] Connect to OpenAI / Gemini API for smarter replies
- [ ] Remember conversation history
- [ ] Weather API integration
- [ ] Wikipedia search integration
- [ ] Light / Dark mode toggle
- [ ] Mobile PWA support (works offline like an app)

---

## 🤝 Contributing

Want to make Friday smarter? Contributions are welcome!

```bash
# 1. Fork this repository
# 2. Create your feature branch
git checkout -b feature/smarter-replies

# 3. Make your changes
# 4. Commit with a clear message
git commit -m "Add: weather API integration"

# 5. Push and open a Pull Request
git push origin feature/smarter-replies
```

---

## 📄 License

This project is licensed under the **MIT License** — free to use, modify, and distribute with credit.

---

## 📬 Contact

**Sandesh**

[![GitHub](https://img.shields.io/badge/GitHub-@sandesh-black?style=flat&logo=github)](https://github.com/YOUR_USERNAME)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://linkedin.com/in/YOUR_PROFILE)

---

<div align="center">

⭐ **If you like Friday, give this repo a star!** ⭐

*Built with ❤️ and JavaScript by Sandesh*

</div>
