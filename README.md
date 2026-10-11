# CyberLearn AI v4.0

**An Autonomous Cybersecurity Learning Assistant Powered by Local AI**

CyberLearn AI is a Python-based cybersecurity research assistant that autonomously explores web resources, extracts security-related information, summarizes articles using a local AI model, and stores its findings in a persistent knowledge base.

Built with Python and Ollama, CyberLearn AI is designed for cybersecurity enthusiasts, ethical hacking learners, and anyone interested in exploring security concepts and tools.

## ✨ Features

- **Autonomous Web Crawling** — Discovers and visits cybersecurity-related web pages.
- **AI-Powered Summarization** — Uses a local Ollama model to summarize web content.
- **Persistent Knowledge Base** — Saves collected information, summaries, and conversation history locally.
- **Automatic Website Discovery** — Finds new links and discovers additional sources through search engines.
- **Custom Website Sources** — Add your own websites and choose whether to explore their internal pages.
- **Kali Linux Tool Knowledge** — Learns and organizes information about tools across multiple cybersecurity categories.
- **Interactive AI Chat** — Ask questions about cybersecurity and previously collected information.
- **Topic-Based Research** — Search for specific cybersecurity topics and queue relevant pages.
- **Terminal Interface** — Provides a colorful command-line interface using Rich.
- **Logging and Statistics** — Records activity and tracks collected knowledge.
- **Robots.txt Support** — Respects website crawling rules for automatically discovered sources, with an exception for manually supplied sources.

## 🛠️ Technologies

- Python 3
- Ollama
- Local large language models (LLMs)
- Requests
- Beautiful Soup 4
- Rich
- Colorama
- lxml

## 📋 Requirements

Before running CyberLearn AI, make sure you have:

- Python 3.10 or newer recommended
- [Ollama](https://ollama.com/) installed
- A compatible Ollama model downloaded
- An active internet connection for web research
- Enough system memory to run your selected AI model

## 🚀 Installation

### 1. Clone the repository

```bash
git clone https://github.com/whitebuss7/-CyberLearn-AI-v4.0.git
cd -CyberLearn-AI-v4.0
```

Replace `YOUR-USERNAME` with your GitHub username and `CyberLearn-AI` with your repository name if different.

### 2. Install Python dependencies

```bash
python -m pip install requests colorama rich beautifulsoup4 lxml
```

### 3. Install and start Ollama

Download Ollama from:

https://ollama.com/

Pull the default model:

```bash
ollama pull llama3.2
```

Make sure the Ollama service is running before launching the application.

### 4. Run CyberLearn AI

If your Python file is named `hell-.py`:

```bash
python cyberlearn_ai.py
```

On some Linux systems, use `python3` instead of `python`.

## ⚙️ Configuration

CyberLearn AI supports environment variables for configuring the local AI service and model.

### Change the Ollama model

Linux/macOS:

```bash
export CYBER_MODEL=llama3.2
```

Windows PowerShell:

```powershell
$env:CYBER_MODEL = "llama3.2"
```

Replace `llama3.2` with another model installed in Ollama.

### Change the Ollama server URL

Linux/macOS:

```bash
export OLLAMA_URL=http://localhost:11434
```

Windows PowerShell:

```powershell
$env:OLLAMA_URL = "http://localhost:11434"
```

The default URL is `http://localhost:11434`.

## 💻 Available Commands

CyberLearn AI includes an interactive command-line interface.

| Command | Description |
|---|---|
| `oku <url>` | Read and summarize a specific web page |
| `site ekle <url>` | Add a website as a persistent source |
| `site ekle <url> tek` | Add a single page without exploring its internal pages |
| `site sil <url>` | Remove a manually added source |
| `siteler` | View configured website sources |
| `kesfet` | Trigger topic and website discovery |
| `ara <topic>` | Search for a topic and queue relevant pages |
| `domainler` | View discovered domains |
| `kali` | List learned Kali Linux tools |
| `kali <category>` | Filter tools by category or name |
| `arac <name>` | View or learn about a specific tool |

**Example:**

```text
oku https://owasp.org/www-project-top-ten/
ara web application security
arac nmap
kali bilgi_toplama
```

Commands are entered in the application's interactive terminal after startup.

## 🌐 Adding Custom Websites

CyberLearn AI creates a `siteler.txt` file for custom sources.

Add one URL per line:

```text
https://owasp.org/
https://portswigger.net/web-security
https://cheatsheetseries.owasp.org/
```

By default, the crawler can explore additional pages on the supplied website.

To process only a single page, append `tek`:

```text
https://example.com/security-article tek
```

The application checks this file for changes while running.

## 🧠 Local Data and Memory

CyberLearn AI maintains several local files:

| File | Purpose |
|---|---|
| `cyber_brain.json` | Persistent knowledge base, summaries, history, and statistics |
| `cyber_log.txt` | Application logs |
| `siteler.txt` | Custom website sources |

These files may be created automatically during execution.

**Important:** Back up your knowledge base before deleting or modifying its contents.

## 🔐 Privacy

AI inference is performed through the configured Ollama server, which defaults to a local service.

However, CyberLearn AI makes HTTP requests to external websites and search engines to retrieve content. Therefore, it is not completely offline, and your network provider or visited websites may observe network activity.

## ⚠️ Limitations

- AI-generated summaries and answers may contain errors.
- Some websites block automated requests or require JavaScript to render their content.
- Search engine HTML structures may change, affecting discovery.
- Model performance depends on your hardware and the selected Ollama model.
- The application collects information from web pages; it does not guarantee that information is complete, current, or verified.
- The predefined Kali Linux tools are used as a knowledge catalog. CyberLearn AI is not intended to execute those tools automatically.

## ⚖️ Responsible Use

CyberLearn AI is intended for cybersecurity education, research, and authorized security work.

- Respect website terms of service and applicable laws.
- Obtain authorization before testing systems you do not own.
- Do not use collected information to compromise systems or access data without permission.
- Review the behavior of the application before running it in sensitive environments.

## 🤝 Contributing

Contributions, bug reports, feature requests, and improvements are welcome.

1. Fork this repository.
2. Create a feature branch.
3. Make your changes.
4. Test your changes locally.
5. Open a pull request with a clear description.

## 📄 License

No license has been specified yet.

## 👨‍💻 Author

Created by **Aİ**

GitHub: https://github.com/YOUR-USERNAME

---

If you find this project useful, consider giving the repository a ⭐ star!

**CyberLearn AI — Explore. Learn. Understand Security.**
