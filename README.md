# DuckMind

**DuckMind** is an agentic AI platform that shifts you from *getting answers* to **actually getting things done**.  
Instead of just chatting with AI, DuckMind lets the agent **access data, plan, and execute multi-step tasks** — so you can hand off work and come back when it's finished.

DuckMind is designed as an **AI coworker** that runs on your machine. It handles complex tasks end-to-end: breaking them down, executing each step in sequence, and delivering real output.

---

# From Answers to Action

DuckMind doesn't just answer questions.  
It **does the work**.

You describe the goal. DuckMind will:

- analyze the task
- break it into steps
- execute each step
- report progress
- deliver the final result

You can watch it run in real time — or hand it off and come back later.

---

# How DuckMind Works

DuckMind runs on an **agentic workflow** model.

1. Understand the user's goal
2. Decompose it into subtasks
3. Plan the execution
4. Fetch the required data
5. Execute each step
6. Synthesize the final output

Along the way, DuckMind can:

- read files
- analyze data
- write code
- generate reports
- build slide decks
- aggregate information from multiple sources

---

# Automate Repetitive Work

DuckMind shines on time-consuming, recurring tasks.

You can schedule a task to run:

- daily
- weekly
- monthly

Examples:

- compile a morning briefing report
- run periodic data analysis
- aggregate customer feedback
- auto-generate dashboards or presentations

---

# Installation

## 🪟 Windows 11 (WSL + Ubuntu)

DuckMind runs best on Linux. On Windows, install WSL and Ubuntu first.

### Step 1 — Install WSL and Ubuntu

Open **PowerShell** or **Windows Terminal** as **Administrator** and run:

```powershell
wsl --install
```

This command will automatically:
- Enable Windows Subsystem for Linux
- Enable the Virtual Machine Platform
- Install the WSL2 kernel
- Install the latest Ubuntu (typically Ubuntu 24.04 LTS)

Once complete, **restart your machine**.

### Step 2 — Install Ubuntu 24.04 from the Microsoft Store

1. Open **Microsoft Store** (search in Start Menu).
2. Search for **Ubuntu 24.04**.
3. Select **Ubuntu 24.04.1 LTS** and click **Get** or **Install**.
4. Wait for the download to finish (a few hundred MB).

---

### Step 3 — Initialize Ubuntu for the First Time

1. Open **Tabby** (recommended for Unicode/Vietnamese input) or launch **Ubuntu 24.04** as **Administrator** from the Start Menu.
2. Wait a few minutes for the initial decompression (first launch only).
3. Set a **UNIX username**
   - lowercase only
   - no accents
   - no spaces
4. Set a **password**
   - characters will not appear as you type — this is expected behavior.

---

### Step 4 — Set Up the Environment Inside Ubuntu

Open the Ubuntu terminal and run the following in order:

**Update the system**
```bash
sudo apt update && sudo apt upgrade -y
```

**Install system packages**
```bash
sudo apt install -y \
  git \
  python3 python3-pip python3-venv \
  build-essential \
  coreutils \
  libreoffice \
  poppler-utils \
  curl
```

**Install Node.js 22 LTS**
```bash
curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt install -y nodejs
```

Verify:
```bash
node -v
npm -v
```

**Install Python packages**
```bash
pip3 install --break-system-packages markitdown Pillow openpyxl
```

**Install DuckMind**
```bash
sudo npm install -g @duckmind/dm docx xlsx pptxgenjs
```

**Verify installation**
```bash
git --version
python3 --version
node -v && npm -v
dm --version
```

---

## 🐧 Linux Ubuntu

On Ubuntu, you can install DuckMind directly without WSL.

### Step 1 — Update the system
```bash
sudo apt update && sudo apt upgrade -y
```

### Step 2 — Install system packages
```bash
sudo apt install -y \
  git \
  python3 python3-pip python3-venv \
  build-essential \
  coreutils \
  libreoffice \
  poppler-utils \
  curl
```

### Step 3 — Install Node.js 22 LTS
```bash
curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt install -y nodejs
```

Verify:
```bash
node -v
npm -v
```

### Step 4 — Install Python packages
```bash
pip3 install --break-system-packages markitdown Pillow openpyxl
```

### Step 5 — Install DuckMind
```bash
sudo npm install -g @duckmind/dm docx xlsx pptxgenjs
```

### Step 6 — Verify installation
```bash
git --version
python3 --version
node -v && npm -v
dm --version
```

---

## 🍎 macOS

### Step 1 — Install Homebrew

If Homebrew is not already installed:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

If you're on **Apple Silicon (M1/M2/M3/M4)**, add Homebrew to your PATH after installation:
```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

---

### Step 2 — Install Git, Python, and Node.js
```bash
brew update
brew install git python node
```

---

### Step 3 — Install Xcode Command Line Tools
```bash
xcode-select --install
```

> An installation dialog will appear. Click **Install** and wait for it to complete.

---

### Step 4 — Install system utilities
```bash
brew install poppler coreutils
brew install --cask libreoffice
```

---

### Step 5 — Install Python packages
```bash
pip3 install markitdown Pillow openpyxl
```

---

### Step 6 — Install DuckMind
```bash
npm install -g @duckmind/dm docx xlsx pptxgenjs
```

---

### Step 7 — Verify installation
```bash
git --version
python3 --version
node -v && npm -v
dm --version
```

---

# Getting Started with the DuckMind CLI

After installation, open a terminal and run:
```bash
dm
```
The CLI will start in interactive mode.

---

### Connect a Model

Inside the CLI, type:
```bash
/login
```
Select the **DuckMind** provider from the list.

### Enter Your API Key

After selecting a provider, the CLI will prompt:
```bash
Enter API key: sk-xxxx
```
Paste your API key and press Enter.

### Select a Mode

DuckMind offers four modes:

| Mode  | Description |
|-------|-------------|
| Free  | Limited access |
| Lite  | Fast, token-efficient |
| Smart | Fast and capable — suitable for most tasks |
| Deep  | Deep reasoning — for complex, multi-step problems |

**Recommendation:** Default to **Smart**. Switch to **Deep** only when the task demands intensive reasoning.
