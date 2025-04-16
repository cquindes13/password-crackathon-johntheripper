# 🔐 Week 3 – Password Crack-a-thon  
## CodePath Cybersecurity | Spring 2025

This repository contains my submission for **Week 3** of CodePath’s Cybersecurity course. The project simulates real-world password hash cracking using John the Ripper and a fictional leaked dataset, modeled after incidents like the LinkedIn and Yahoo data breaches.

---

## 📁 Contents
- 📄 Project submission (PDF/Docx)
- 📸 Screenshot: Total number of passwords cracked
- 💻 Sample John the Ripper commands using:
  - A custom wordlist
  - Built-in ruleset
  - Custom mask

---

## 🎯 Learning Objectives
By the end of this project, I was able to:
- ✅ Use John the Ripper to crack password hashes
- ✅ Work with custom and built-in wordlists
- ✅ Use rule sets and masks to improve cracking success
- ✅ Understand how password length and entropy affect security

---

## 🧪 Project Details

### 📊 Total Passwords Cracked
**📸 Screenshot Included**  
✅ **254 password hashes cracked** out of 1000 (25.4%)

---

### 💻 Commands Used

**🔹 Command #1: Using a custom wordlist (rockyou.txt)**  

john --format=md5crypt-long --wordlist=/usr/share/wordlists/rockyou.txt cp_leak.txt

---


**🔹 Command #2: Using a built-in ruleset (best64)**

john --format=md5crypt-long --wordlist=/usr/share/wordlists/rockyou.txt --rules=best64 cp_leak.txt

---
**🔹 Command #3: Using a custom mask**

john --format=md5crypt-long --mask=?l?l?l?l?d?d cp_leak.txt

---
**Alternate mask:**

john --format=md5crypt-long --mask=?l?l?l?l?l?d cp_leak.txt

---

**💬 Reflection**
Q1: Password security in 3 emojis
🧐 🤗 🥳

---

**🛡️ Q2: What makes a password hash hard to crack?**

Password hashes are harder to crack when:

They have high entropy (randomness & length)

Are salted, to prevent rainbow table attacks

Use key stretching (like PBKDF2 or Argon2)

While websites require complex passwords, many don’t implement strong hashing methods, leaving them vulnerable to offline brute-force or dictionary attacks.

---

**🙌 Shoutouts**

Thanks to:

Google & AI tools 🤖

Hints provided in the course portal

John the Ripper documentation

---

**🧠 Author Info**

Name: Cristian Quindes

Email: quindes1352@gmail.com

Course: CYB101 – CodePath Cybersecurity Spring 2025
