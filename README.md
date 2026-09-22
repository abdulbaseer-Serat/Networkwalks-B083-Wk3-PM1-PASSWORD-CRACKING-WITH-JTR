<div align="center">

# 🔐 Cybersecurity & Ethical Hacking — Practical Project Modules 

![Cybersecurity](https://img.shields.io/badge/Domain-Cybersecurity-critical?style=for-the-badge&logo=hackaday&logoColor=white)
![Kali Linux](https://img.shields.io/badge/OS-Kali%20Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![Python](https://img.shields.io/badge/Language-Python%203-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Claude Desktop](https://img.shields.io/badge/AI-Claude%20Desktop-D97757?style=for-the-badge&logo=anthropic&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

*A hands-on documentation of my cybersecurity learning journey — from password hashing to AI‑assisted security automation.*

</div>

---

## 📌 Overview

This repository documents my hands-on learning journey through practical **Cybersecurity & Ethical Hacking Project Modules**, provided by **Networkwalks Academy**.

The modules focused on moving beyond theory into real, practical exposure to:

- 🔑 Password security & hashing
- 🧠 Wordlist-based password cracking
- 🐧 Linux security environments
- 🤖 AI-assisted security tooling
- 🔗 MCP-based security automation

> ⚠️ All work was performed in a **controlled lab/learning environment**, strictly for educational and cybersecurity training purposes.

---

## 🗂️ Table of Contents

- [🧪 Module 1 — Cybersecurity Practical Tasks](#-module-1--cybersecurity-practical-tasks)
- [🔓 Module 2 — Password Cracking with NetworkWalks Tools](#-module-2--password-cracking-with-networkwalks-tools)
- [🤖 Module 3 — Setting Up HexStrike MCP with Claude](#-module-3--setting-up-hexstrike-mcp-with-claude)
- [🧠 Overall Learning](#-overall-learning)
- [🛠️ Technologies & Tools](#️-technologies--tools)
- [📈 Learning Journey](#-learning-journey)
- [🏁 Conclusion](#-conclusion)
- [🙏 Acknowledgement](#-acknowledgement)
- [⚠️ Disclaimer](#️-disclaimer)

---

## 🧪 Module 1 - Task 1: PDF Password Cracking Using a CLI-Based Dictionary Attack.
### CLI-Based PDF Password Recovery Using a Dictionary Attack

A command-line approach for recovering authorized PDF passwords by extracting PDF hashes with `pdf2john` and testing candidate passwords using `John the Ripper` and a wordlist-based dictionary attack.

<div align="center">
   <img width="1105" height="391" alt="image" src="https://github.com/user-attachments/assets/69b85fd0-bafb-40d3-ba82-1541207c43f9" />
 
   📸 *Screenshot: PDF Password Cracking Using a CLI-Based Dictionary Attack*
</div>

### Reusability of the Workflow

The same CLI-based password recovery workflow can be applied to other authorized password-protected PDF files by extracting the PDF hash with `pdf2john` and performing a dictionary attack using `John the Ripper` with an appropriate wordlist.

### Generic Commands

1. Extract the PDF hash:

```bash
pdf2john "filename.pdf" > hash.txt
like: pdf2john "$HOME/Desktop/My Locked PDF1.pdf" > "$HOME/Desktop/hash1.txt"
```
2. cat "$HOME/Desktop/hash1.txt" or cat hash.txt
3. Run a dictionary attack using a wordlist:
```bash
john --format=pdf --wordlist=rockyou.txt hash.txt
like: john --format=pdf --wordlist="$HOME/Desktop/rockyou.txt" hash1.txt
```
4. Display the recovered password:
```bash
john --show --format=pdf hash.txt
```

## 🧪 Module 1 - Task 2: PDF Password Cracking Using Johnny (GUI)
Recover the password of an authorized password-protected PDF using Johnny, the graphical user interface (GUI) for John the Ripper.

### Tools Used
- Johnny (GUI for John the Ripper)
- PDF Hash Extractor (Online Hash Crack PDF Hash Extractor)

## Procedure
1. Open the hash website & upload your pdf file to find its hash (https://www.onlinehashcrack.com/tools-pdf-hash-extractor.php).
2. Copy the extracted PDF hash, and Paste the hash value inside notepad. save it as txt e.g. hash.txt
3. Open Johnny. Click on ‘Open password file, and Browse to the hash1.txt file that you have just saved & click on Open
4. Click on ‘Start new attack’ - *Your PDF file password will be cracked (it might take some time depending on your computer 
speed & password complexity):*

<div align="center">
<img width="1471" height="903" alt="image" src="https://github.com/user-attachments/assets/31db849f-42ed-48cb-bbbe-b53e570ba792" />

   📸 *Screenshot: PDF Password Cracking Using Johnny (GUI)*
</div>


## 🔓 Module 2 — Password Cracking with NetworkWalks Tools

### 🎯 Objective
Gain practical experience with password hashing, hash analysis, and password recovery using the NetworkWalks Hash Calculator and Password Cracker in a controlled training environment.

### 🛠️ Tools Used
- 🧮 NetworkWalks Hash Calculator
- 🔓 NetworkWalks Password Cracker
- 📄 Password-protected PDF (`My Locked PDF1.pdf`)

### 📋 Procedure

1. Upload the protected PDF to the Hash Calculator.
2. Extract and copy the PDF hash.
3. Import the hash into the Password Cracker.
4. Run a dictionary-based password recovery process. or click on " Start Crack"
5. Recover and verify the password.

### ✅ Screenshots and Results
<div align="center">
<img width="958" height="494" alt="image" src="https://github.com/user-attachments/assets/db78ddcb-e96a-45c8-9e70-ea304c8a7119" />

   📸 *Screenshot: Hash Calculator*
</div>
<div align="center">
<img width="957" height="499" alt="image" src="https://github.com/user-attachments/assets/20b51099-5a98-41cb-acfd-38603ee38b3e" />

   📸 *Screenshot: Password Cracker through Dictionary Attacks*
</div>

### 🧪 Key Learning Outcomes

- ✅ How password hashing works at a practical level
- ✅ How different hashing algorithms produce different hash values
- ✅ How hashes can be used as inputs during password-recovery attacks
- ✅ How dictionary/wordlist-based password cracking works
- ✅ Why weak and predictable passwords are easier to recover
- ✅ The importance of strong password policies and secure password-storage mechanisms
- ✅ How cybersecurity training environments use flags to verify successful exploitation or challenge completion

### 🔐 Security Takeaways

- 🔓 Weak passwords can be recovered relatively easily when they appear in common wordlists
- 🛡️ Password hashes should be protected even though they are not plaintext passwords
- ⚠️ Legacy hashing algorithms such as MD5 and SHA-1 are unsuitable for modern password storage
- 💪 Strong, unique passwords significantly increase resistance to dictionary-based attacks
- 🧂 Modern password storage should use dedicated password-hashing mechanisms with appropriate salting and work factors

### ⚠️ Ethical Consideration

All password-cracking activities in this module were performed in a controlled cybersecurity training environment provided for educational purposes. Password cracking should only be performed on systems, accounts, files, or hashes for which **explicit authorization** has been provided.


---

## 🤖 Module 3 — Setting Up HexStrike MCP with Claude
<img width="1600" height="840" alt="claude" src="https://github.com/user-attachments/assets/f4d61ea0-7648-4161-ac42-5315d9f82566" />
<img width="656" height="489" alt="hexstrike2" src="https://github.com/user-attachments/assets/65e72d97-2173-44a7-998e-5996d4ad834a" />
<img width="661" height="489" alt="hexstrike" src="https://github.com/user-attachments/assets/3ffd997f-b088-4e4c-8fd3-10f30e6dca32" />

### 🎯 Objective

Set up the **HexStrike MCP Server** with **Claude Desktop** inside a **Kali Linux** environment, exploring how an MCP-based architecture connects an AI assistant with locally running security tooling.

### 🖥️ Environment

| Component | Detail |
|---|---|
| **OS** | Kali Linux |
| **AI Assistant** | Claude Desktop |
| **Security Platform** | HexStrike AI |
| **Protocol** | MCP |
| **Server** | Localhost |
| **Port** | `8888` |

### 🐉 HexStrike AI

Configured as the local security-tool server, providing an MCP-based interface to multiple security tools.

### 🖥️ Step 1 — Claude Desktop Setup

- 🔑 Added the required GPG key
- 📦 Added the Claude Desktop repository
- 🔄 Updated package repositories
- ⬇️ Installed Claude Desktop
- 🚀 Launched and signed in

### 📥 Step 2 — Downloading HexStrike AI

```bash
git clone <hexstrike-ai-repo>
# Project directory: /home/arshiya/hexstrike-ai
```

### 🐍 Step 3 — Python Virtual Environment

```bash
python3 -m venv hexstrike-env
source hexstrike-env/bin/activate
```

### 📦 Step 4 — Installing Dependencies

```bash
pip3 install -r requirements.txt
```

### 🚀 Step 5 — Starting the HexStrike Server

```bash
cd ~/hexstrike-ai
source hexstrike-env/bin/activate
python3 hexstrike_server.py
```

**Output confirmed:**
```
[INFO] Server starting on 127.0.0.1:8888
Running on http://127.0.0.1:8888
```

### ⚙️ Step 6 — MCP Configuration

```
Claude Desktop
      │
      │ MCP
      ▼
hexstrike_mcp.py
      │
      ▼
localhost:8888
      │
      ▼
HexStrike AI Server
```

### 🔗 Step 7 — HexStrike MCP Connection

```
hexstrike-env/bin/python
        ↓
hexstrike_mcp.py
        ↓
--server
        ↓
http://localhost:8888
```

### ✅ Step 8 — Server Verification

```
Serving Flask app 'hexstrike_server'
Debug mode: off
Running on all addresses (0.0.0.0)
Running on: http://127.0.0.1:8888
```

### 🧩 Architecture

```
                    ┌──────────────────┐
                    │  Claude Desktop  │
                    └────────┬─────────┘
                             │ MCP
                             ▼
                    ┌──────────────────┐
                    │ hexstrike_mcp.py │
                    └────────┬─────────┘
                             │ HTTP
                             ▼
                    ┌──────────────────┐
                    │ HexStrike Server │
                    │   Port: 8888     │
                    └────────┬─────────┘
                             ▼
                    ┌──────────────────┐
                    │ Security Tools   │
                    │ & Analysis       │
                    └──────────────────┘
```

### 🔍 What I Learned

- ✅ MCP architecture
- ✅ AI-to-tool integration
- ✅ Local security-tool infrastructure
- ✅ Python virtual environments
- ✅ Dependency management
- ✅ Linux-based security environments
- ✅ Flask-based server execution
- ✅ Connecting AI assistants with local tooling

---

## 🧠 Overall Learning

<table>
<tr>
<th>🧪 Module 1</th>
<th>🔓 Module 2</th>
<th>🤖 Module 3</th>
</tr>
<tr>
<td>

```
Security Concepts
      ↓
Hashing
      ↓
Password Security
      ↓
Password Cracking
      ↓
CTF / Flag Capture
```

</td>
<td>

```
Hash Generation
      ↓
Hash Algorithms
      ↓
Provide Hash to Cracker
      ↓
Wordlist Attack
      ↓
Password Recovered
      ↓
Flag Capture
```

</td>
<td>

```
Linux Environment
      ↓
Python Environment
      ↓
Security Tool Server
      ↓
MCP
      ↓
Claude Desktop
      ↓
AI-Assisted Workflow
```

</td>
</tr>
</table>

---

## 🛠️ Technologies & Tools

<div align="center">

![Kali Linux](https://img.shields.io/badge/-Kali%20Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white)
![Python](https://img.shields.io/badge/-Python%203-3776AB?style=flat-square&logo=python&logoColor=white)
![Claude](https://img.shields.io/badge/-Claude%20Desktop-D97757?style=flat-square&logo=anthropic&logoColor=white)
![Flask](https://img.shields.io/badge/-Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Git](https://img.shields.io/badge/-Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/-GitHub-181717?style=flat-square&logo=github&logoColor=white)
![MCP](https://img.shields.io/badge/-MCP-6C63FF?style=flat-square)
![HexStrike AI](https://img.shields.io/badge/-HexStrike%20AI-FF4B4B?style=flat-square)

</div>

- 🐧 Kali Linux
- 🐍 Python 3
- 🖥️ Claude Desktop
- 🔗 MCP
- 🐉 HexStrike AI
- ⚗️ Flask
- 🧮 Networkwalks Hash Calculator
- 🔓 Networkwalks Password Cracker
- 📚 Wordlists
- 🌱 Git & GitHub

---

## 📈 Learning Journey

```
Cybersecurity Fundamentals
          ↓
Password Security
          ↓
Hashing
          ↓
Password Cracking
          ↓
Wordlists
          ↓
Hash Generation & Analysis
          ↓
Capture The Flag
          ↓
Linux Security Environment
          ↓
Python Virtual Environment
          ↓
HexStrike AI
          ↓
MCP
          ↓
Claude Desktop
          ↓
AI-Assisted Cybersecurity 🔐🤖
```

> From understanding attacks → to understanding tools → to connecting AI with security tooling.

---

## 🏁 Conclusion

These practical modules were a significant part of my cybersecurity learning journey. From understanding how password hashes can be extracted and tested in controlled environments, to generating and cracking hashes with the **NetworkWalks tools**, to setting up an MCP-based security environment with **Claude Desktop** and **HexStrike AI** — the exercises provided valuable hands-on exposure to modern cybersecurity workflows.

More importantly, this experience reinforced the value of **learning by doing** — understanding the underlying technology and continuously developing a practical security mindset.

---


## ⚠️ Disclaimer

> All activities documented in this repository were performed as part of **authorized cybersecurity training** and **controlled laboratory exercises**.
>
> The techniques and tools discussed should only be used on systems, files, networks, and environments where **explicit authorization** has been provided.

---

<div align="center">

### 🔐 Prepared by **Abdulbaseer Serat** 🤖

⭐ *If you found this useful, consider giving this repo a star!* ⭐

</div>
