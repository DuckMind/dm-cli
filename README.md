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

## System Requirements

DuckMind runs on the following platforms and configurations:

**Operating system:**
- macOS 13.0+
- Windows 10 1809+ or Windows Server 2019+
- Ubuntu 20.04+
- Debian 10+
- Alpine Linux 3.19+

**Hardware:** 4 GB+ RAM, x64 or ARM64 processor

**Network:** Internet connection required. See [network configuration](#network-configuration).

**Shell:** Bash, Zsh, PowerShell, or CMD.

---

## 🪟 Windows 11 (WSL + Ubuntu)

DuckMind runs inside WSL (Windows Subsystem for Linux). Complete the following steps to set up WSL and Ubuntu, then use the Quick Install above.

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

### Step 3 — Initialize Ubuntu for the First Time

1. Open **Tabby** (recommended for Unicode/Vietnamese input) or launch **Ubuntu 24.04** as **Administrator** from the Start Menu.
2. Wait a few minutes for the initial decompression (first launch only).
3. Set a **UNIX username**
   - lowercase only
   - no accents
   - no spaces
4. Set a **password**
   - characters will not appear as you type — this is expected behavior.

### Step 4 — Install DuckMind

Inside the Ubuntu terminal, run:

```bash
curl -fsSL https://get.duckmind.dev | bash
```

Verify:

```bash
dm --version
```

---

## 🐧 Linux Ubuntu

```bash
curl -fsSL https://get.duckmind.dev | bash
```

Verify:

```bash
dm --version
```

---

## 🍎 macOS

```bash
curl -fsSL https://get.duckmind.dev | bash
```

Verify:

```bash
dm --version
```

---

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
