# Ai-Agent

# 🌐 Browser-Use Web UI – AI-Powered Browser Agent

Browser-Use Web UI is an interactive, Gradio-based interface for running AI agents that can browse and interact with websites autonomously. It builds on the browser-use framework and supports persistent sessions, custom browsers, and multiple LLMs including OpenAI, Gemini, DeepSeek, Anthropic, Azure, and Ollama.

## 🚀 Features
- Interactive Web UI using Gradio
- Supports OpenAI, Gemini, DeepSeek, Ollama, etc.
- Persistent browser sessions
- Use your local Chrome with saved logins
- Docker and local setup supported
- Live monitoring via built-in VNC viewer

## 🔧 Installation

### Option 1: Local Setup
```bash
git clone https://github.com/browser-use/web-ui.git
cd web-ui
python3 -m venv .venv
source .venv/bin/activate  # or .\.venv\Scripts\activate for Windows
pip install -r requirements.txt
playwright install --with-deps
cp .env.example .env  # Fill in your API keys
python webui.py --ip 127.0.0.1 --port 7788
  Access it at: http://127.0.0.1:7788

Option 2: Docker Setup
bash
Copy
Edit
git clone https://github.com/browser-use/web-ui.git
cd web-ui
cp .env.example .env
docker compose up --build
For ARM64 (Apple Silicon):

bash
Copy
Edit
TARGETPLATFORM=linux/arm64 docker compose up --build
Optional: Use Your Own Chrome
Set the following in .env:

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
📺 VNC Viewer
Open http://localhost:6080/vnc.html to watch your agent in action (default password: youvncpassword).

📚 Supported Models
OpenAI (gpt-3.5, gpt-4)

Google Gemini

DeepSeek

Azure OpenAI

Anthropic (Claude)

Ollama
