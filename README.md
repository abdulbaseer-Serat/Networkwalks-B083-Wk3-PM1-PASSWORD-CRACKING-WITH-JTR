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

## 🧪 Module 1 - Task 1: PDF Password Recovery Using a CLI-Based Dictionary Attack.
### CLI-Based PDF Password Recovery Using a Dictionary Attack

A command-line approach for recovering authorized PDF passwords by extracting PDF hashes with `pdf2john` and testing candidate passwords using `John the Ripper` and a wordlist-based dictionary attack.

<img width="1105" height="391" alt="image" src="https://github.com/user-attachments/assets/69b85fd0-bafb-40d3-ba82-1541207c43f9" />

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
## 🧪 Module 1 - Task 2: PDF Password Recovery Using Johnny (GUI)
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

<img width="1471" height="903" alt="image" src="https://github.com/user-attachments/assets/31db849f-42ed-48cb-bbbe-b53e570ba792" />


### 🎯 Objective

Gain practical exposure to fundamental cybersecurity concepts through hands-on security challenges, including password security, hashing, wordlists, and CTF-style problem solving.

**Skills covered:**

| 🧩 Area | 📖 Focus |
|---|---|
| Cybersecurity Fundamentals | Core concepts & terminology |
| Security Testing Methodology | Structured problem solving |
| Password Security | Weak vs. strong passwords |
| Hashing Concepts | One-way transformations |
| Wordlists | Dictionary-based attacks |
| Password Cracking | Practical recovery workflow |
| CTF Challenges | Flag-based validation |

### 🔑 Password Security & Hashing

Passwords aren't usually stored directly — instead, systems rely on **cryptographic hashes**, a one-way transformation producing a fixed-format representation of the original input.

**Practical workflow:**

```
Protected File
     ↓
Hash Extraction
     ↓
Hash Identification
     ↓
Password Cracking
     ↓
Password Recovery
     ↓
Access to Protected File
```

### 🧰 Networkwalks Password Cracker

Practiced against a lab file: `My Locked PDF1.pdf`

**Steps followed:**

1. 📥 Download the encrypted lab PDF
2. 🧮 Open the Networkwalks Hash Calculator
3. 📤 Upload the protected PDF
4. 🔍 Extract the PDF hash
5. 📋 Copy the hash (starting with `$pdf$`)
6. 🖥️ Open the Networkwalks Password Cracker
7. 📝 Provide the extracted hash
8. ▶️ Start the cracking process
9. ⏳ Wait for password recovery
10. 🔓 Use the recovered password to open the PDF

### 🧠 Wordlists & Password Cracking

Password-cracking effectiveness depends on:

- 📏 Password length
- 🔀 Password complexity
- 🎯 Password predictability
- 📚 Wordlist quality
- 🔡 Character combinations
- 🌐 Search space
- ⚡ Available computing resources

> 💡 **Key takeaway:** Weak and predictable passwords are significantly easier to recover than strong, unique ones.

### 🚩 Captured Flags

```
🏁 nw[networkwalks_flag_260821_1]
🏁 nw[networkwalks_persistence_jtr_270521]
🏁 nw[cybersecurity_flag_captured_2608]
```

### 📚 Key Learning Outcomes

- ✅ Password security fundamentals
- ✅ Hashing concepts
- ✅ Password recovery techniques
- ✅ Wordlist-based attacks
- ✅ Practical cybersecurity investigation
- ✅ Capture-the-Flag methodology
- ✅ Understanding weak-password risks

---

## 🔓 Module 2 — Password Cracking with NetworkWalks Tools
<img width="1600" height="840" alt="hashcalculator" src="https://github.com/user-attachments/assets/e94157ee-48df-4928-b731-518c915f9b5e" />
<img width="1600" height="840" alt="pass cracker" src="https://github.com/user-attachments/assets/35877680-6694-45c4-9fff-a817b72985b7" />

### 📌 Overview

In this module, I worked on password cracking using the **NetworkWalks password-cracking tools**. The practical focused on understanding how password hashes are generated/extracted and how those hashes can be tested against password wordlists to recover the original password.

The complete workflow was performed in a controlled cybersecurity training environment for learning and ethical-security purposes.

### 🎯 Objectives

- 🔎 Understand the concept of password hashing
- 🧮 Generate/extract password hashes using the NetworkWalks Hash Calculator
- 🧠 Understand commonly used hash algorithms such as MD5 and SHA-1
- 🔗 Use the generated hash as input for password cracking
- 📚 Perform dictionary-based password cracking using the NetworkWalks Password Cracker
- ✅ Verify the recovered password
- 🚩 Successfully capture the provided training flag

### 🧠 Concept — Password Hashing

A password hash is a fixed-length representation generated from a password using a hashing algorithm.

During the practical, the **NetworkWalks Hash Calculator** was used to generate hashes from text, providing outputs for algorithms including:

| Algorithm | Notes |
|---|---|
| MD5 | ⚠️ Legacy — not secure for passwords |
| SHA-1 | ⚠️ Legacy — not secure for passwords |
| SHA-256 | ✅ Stronger |
| SHA-384 | ✅ Stronger |
| SHA-512 | ✅ Stronger |

> 💡 The practical demonstrated that older algorithms such as MD5 and SHA-1 should not be considered secure choices for storing passwords.

### 🛠️ Tools Used

- 🧮 **NetworkWalks Hash Calculator** — used to generate password hashes and work with hash values.
- 🔓 **NetworkWalks Password Cracker** — used to attempt recovery of the original password from its hash using a wordlist-based approach.

### 🔄 Practical Workflow

```text
Input Password/Text
        ↓
NetworkWalks Hash Calculator
        ↓
Generate Hash
        ↓
Identify/Select Hash Type
        ↓
Provide Hash to Password Cracker
        ↓
Use Password Wordlist
        ↓
Cracking Process
        ↓
Password Recovered
        ↓
Verify Result
        ↓
Capture Training Flag
```

### 🔎 Step 1 — Generate the Hash

Text was entered into the **NetworkWalks Hash Calculator**, which generated multiple hash representations of the input, including MD5 and SHA-1.

This helped in understanding how the same input can produce different hash values depending on the hashing algorithm used.

### 🔓 Step 2 — Password Cracking

After obtaining the hash, the **NetworkWalks Password Cracker** was used. The hash was provided to the cracker along with an appropriate password wordlist.

The tool tested candidate passwords against the target hash until a matching password was identified.

**✅ Result:** The password was successfully cracked as:

```
password1
```

### 🚩 Step 3 — Flag Capture

After successfully recovering the password, the corresponding training flag was obtained — confirming the password-cracking workflow was completed successfully.

**Captured flags from this practical:**

```
🏁 nw[networkwalks_flag_260821_1]
🏁 nw[networkwalks_persistence_jtr_270521]
```

### 📸 Practical Evidence

Screenshots were captured during the practical to document:

- 🧮 Hash generation using the NetworkWalks Hash Calculator
- 🔢 Hash values generated for different algorithms
- ⚙️ Password-cracking configuration
- ▶️ Password-cracking process
- ✅ Successful password recovery
- 🚩 Successful flag capture

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

### ✅ Module Status

**Project Module 2 — Completed Successfully 🎯**

`Hash Generation → Hash Analysis → Password Cracking → Password Recovery → Flag Capture`

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
