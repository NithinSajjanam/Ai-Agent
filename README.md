# Ai-Agent

# 🌐 Browser-Use Web UI – AI-Powered Browser Agent

[![Stars](https://img.shields.io/github/stars/browser-use/web-ui?style=social)](https://github.com/browser-use/web-ui)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](#license)
[![Python](https://img.shields.io/badge/built%20with-python-blue.svg)](https://www.python.org/)

---

## 🧠 Overview

**Browser-Use Web UI** is an interactive, Gradio-based front end designed for running **AI agents** that can browse and interact with the web like a human. It extends the capabilities of the [browser-use](https://github.com/browser-use/browser-use) core by enabling persistent browser sessions, visual feedback, and multi-LLM support (including OpenAI, Gemini, DeepSeek, Azure, Ollama, and more).

> Run smart autonomous agents that can click, type, navigate, and reason – right inside your browser!

---

## 🚀 Features

- ✅ Gradio-powered user interface for interactive browser agents
- 🌐 Persistent browser sessions and local Chrome support
- 🔒 Seamless API key management via `.env`
- 📹 Built-in VNC viewer for live session monitoring
- 🤖 Plug-and-play support for LLMs: OpenAI, Google Gemini, DeepSeek, Anthropic, Ollama, etc.
- 🐳 Docker support for easy deployment

---

## 📦 Installation

### 🔧 Option 1: Local Setup

```bash
git clone https://github.com/browser-use/web-ui.git
cd web-ui

Step 1: Create Virtual Environment
bash
Copy
Edit
python3 -m venv .venv
source .venv/bin/activate  # or .\.venv\Scripts\activate on Windows
Step 2: Install Requirements
bash
Copy
Edit
pip install -r requirements.txt
playwright install --with-deps
Step 3: Configure Environment
bash
Copy
Edit
cp .env.example .env  # Add your API keys inside .env
Step 4: Run the Web UI
bash
Copy
Edit
python webui.py --ip 127.0.0.1 --port 7788
Then visit: http://127.0.0.1:7788

🐳 Option 2: Docker Installation
bash
Copy
Edit
git clone https://github.com/browser-use/web-ui.git
cd web-ui
cp .env.example .env  # Add API keys
docker compose up --build
💡 For ARM64 (Apple Silicon):

bash
Copy
Edit
TARGETPLATFORM=linux/arm64 docker compose up --build
💡 Custom Browser Setup (Optional)
Use your own Chrome instance and user profile:

Windows

env
Copy
Edit
BROWSER_PATH="C:\Program Files\Google\Chrome\Application\chrome.exe"
BROWSER_USER_DATA="C:\Users\YourUsername\AppData\Local\Google\Chrome\User Data"
macOS

env
Copy
Edit
BROWSER_PATH="/Applications/Google Chrome.app/Contents/MacOS/Google Chrome"
BROWSER_USER_DATA="/Users/YourUsername/Library/Application Support/Google/Chrome"
🧪 LLM Support
Easily connect to:

OpenAI (GPT-3.5, GPT-4)

Google Gemini

DeepSeek

Azure OpenAI

Anthropic (Claude)

Ollama

More coming soon...

📺 VNC Viewer
View AI agent actions live at:
http://localhost:6080/vnc.html

Default password: youvncpassword (can be changed in .env)

📜 License
This project is licensed under the MIT License.

🙏 Acknowledgements
Thanks to @warmshao, @vvincent1234, and all contributors.

Built with love for the open-source AI community.

🔗 Resources
📘 Documentation

💬 Discord Community

🧠 browser-use core

