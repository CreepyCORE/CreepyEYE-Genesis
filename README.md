# ![CreepyEYE_mini_baner](./PNG/CreepyEYE_mini_baner.png)

![License: MIT](https://img.shields.io/badge/License-MIT-purple) 
![Status: Stable](https://img.shields.io/badge/Status-Stable-green) 
![Version: 1.2](https://img.shields.io/badge/Version-1.2-darkred.svg)
![Python 3.8+](https://img.shields.io/badge/Python-3.8%2B-blue) 
![OS: Windows/Linux/Mac](https://img.shields.io/badge/OS-Windows%20|%20Linux%20|%20Mac-lightgrey)
![Last Commit](https://img.shields.io/github/last-commit/CreepyHunterX/CreepyEYE-Genesis.svg)
![Open Issues](https://img.shields.io/github/issues/CreepyHunterX/CreepyEYE-Genesis.svg)
&nbsp;

## ⚠️ IMPORTANT!
**CreepyEYE Genesis** is an OSINT (Open Source Intelligence) tool for username, email, IP, domain and phone lookups.  
**Use only for ethical purposes! The developers are not responsible for your actions.**

---

| Windows | Linux |
|---------|-------|
| <img src="./PNG/CE_Windows.png" alt="CreepyEYE Genesis - English UI on Windows" width="340"> | <img src="./PNG/CE_Linux.png" alt="CreepyEYE Genesis - English UI on Linux" width="340"> |





## 🛠️ Features

🔎 Username lookup:  
&nbsp;&nbsp;&nbsp;&nbsp;`GitHub`, `X`, `Instagram`, `TikTok`, `Facebook`, `GitLab`, `Bitbucket`, `Reddit`, `Twitch`, `Kaggle`, `Medium`, `SoundCloud`, `Spotify`

📧 Email verification:  
&nbsp;&nbsp;&nbsp;&nbsp;via `Hunter.io`, `EmailRep.io`  
🌐 IP/domain lookup:  
&nbsp;&nbsp;&nbsp;&nbsp;via `IPinfo`, `Shodan`, `AbuseIPDB`, `VirusTotal`, `GreyNoise`, `Whois`  
📱 Phone numbers: `Numverify`  
🧅 Tor routing  
🈯 Language selection menu (`Ukrainian` / `English` / `Russian`)  
🧾 Raw JSON output (menu option `9`, no restart needed)  
💾 Save scan results as JSON to `reports/`  
⚙️ Automatic dependency installation

---

## Screenshots (EN / UA / RU)

| Language | Windows | Linux |
|----------|---------|-------|
| English  | <img src="./PNG/CE_Windows.png" alt="CreepyEYE Genesis - English UI on Windows" width="340"> | <img src="./PNG/CE_Linux.png" alt="CreepyEYE Genesis - English UI on Linux" width="340"> |
| Ukrainian | <img src="./PNG/CE_Windows_ua.png" alt="CreepyEYE Genesis - Ukrainian UI on Windows" width="340"> | <img src="./PNG/CE_Linux_ua.png" alt="CreepyEYE Genesis - Ukrainian UI on Linux" width="340"> |
| Russian  | <img src="./PNG/CE_Windows_ru.png" alt="CreepyEYE Genesis - Russian UI on Windows" width="340"> | <img src="./PNG/CE_Linux_ru.png" alt="CreepyEYE Genesis - Russian UI on Linux" width="340"> |

---

## Installation

1. **Install Python 3.8+**  
   [Download Python](https://www.python.org/downloads/)

2. **Install Git**  
   - Windows: [Download Git](https://git-scm.com/downloads/win)  
   - Linux: `sudo apt update && sudo apt install git`  
   - MacOS: [Download Git](https://git-scm.com/downloads/mac)

3. **Clone the repository**  
   ```sh
   git clone https://github.com/CreepyHunterX/CreepyEYE-Genesis.git
   cd "CreepyEYE-Genesis"
   ```

4. **Install dependencies**  
   ```sh
   pip install -r requirements.txt
   ```

5. **Run the program**  
   ```sh
   python ce_genesis.py
   ```

6. **Run the tests** *(optional, for contributors)*  
   ```sh
   python -m unittest discover -s tests
   ```

---

## API Keys Setup

API keys are stored in `settings/api/api_keys.env`.  
Use **`6. API settings`** to edit the API keys. CreepyEYE creates `api_keys.env` from the template if it doesn't exist, opens it in the default editor and then prompts for a restart to load the new keys. The file can also be edited manually.  
Template placeholders (`your_shodan_api_key`, …) are treated as unset. Supported variables:

- SHODAN_API_KEY  
- IPINFO_TOKEN  
- ABUSEIPDB_KEY  
- HUNTER_API_KEY  
- VIRUSTOTAL_API_KEY  
- NUMVERIFY_API_KEY  
- GREYNOISE_API_KEY  
- EMAILREP_API_KEY  
- WHOIS_API_KEY  

### Where to get the keys

| Service        | API Key URL                               | Purpose                                           |
|----------------|-------------------------------------------|--------------------------------------------------|
| Shodan         | https://www.shodan.io/                    | Scan IPs, devices, open ports                    |
| IPinfo         | https://ipinfo.io/                        | Lookup IP geolocation and ASN info              |
| AbuseIPDB      | https://www.abuseipdb.com/                | Check if IP is reported for malicious activity  |
| Hunter.io      | https://hunter.io/                        | Email verification and domain search            |
| Numverify      | https://numverify.com/                     | Phone number validation                          |
| GreyNoise      | https://greynoise.io/                 | Context on internet scanners / bots             |
| EmailRep.io    | https://emailrep.io/                       | Reputation check of email addresses             |
| WhoisXML API   | https://whoisxmlapi.com/                  | WHOIS data and domain info                        |
| VirusTotal     | https://www.virustotal.com/               | Scan IPs, domains, and files for malware        |


---

## Tor

Start Tor Browser or tor.exe before launching CreepyEYE. If Tor is available, requests are routed through it.

---

## JSON Output

Menu option **`9`** toggles raw JSON output (`JSON output: ON / OFF`). When enabled, each module also prints the raw API response. Useful for debugging and piping module responses to other tools. Takes effect immediately and doesn't affect saved reports.

---

## Reports

After each scan CreepyEYE prompts `Save full report? (y/n)`. On `y`, the report is written to:

```
reports/<target>_<type>_<YYYYMMDD-HHMMSS>.json
```

UTF-8 JSON with the tool version, target and target type, start/finish timestamps (UTC), whether requests were actually routed through Tor, and per-module results. API keys are stripped before writing.

> ⚠️ `reports/` is gitignored: reports contain target data. Don't commit them or attach them to issues/PRs.

---

## Disclaimer

For ethical OSINT only. Use it within the law.

---

## License

[MIT License](LICENSE)

---

## 🧠 CreepyEYE PRO

**CreepyEYE PRO** is the paid desktop edition for **Windows and Linux** with a **lifetime licence**. 37 integrations (bring your own API keys); lookups by email, username, domain, phone, IP, name and photo EXIF; report export; proxy and Tor support. Up to 3 devices per key.

📖 Docs (installation, activation, service list, CLI reference): **[github.com/CreepyCORE/CreepyEYE-PRO](https://github.com/CreepyCORE/CreepyEYE-PRO)**

🛒 **Store: [creepycore.com](https://creepycore.com/store)**

> ℹ️ PRO is closed-source. This repository is the free, open-source **CreepyEYE Genesis**.

---

## 💸 Support CreepyEYE

Donations fund new API integrations, UI/performance work and ongoing updates.

### ☕ Ko-fi
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/F1F71KKMAH)

### 💛 Buy Me a Coffee
[<a href="https://www.buymeacoffee.com/CreepyHunterX" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>](https://buymeacoffee.com/CreepyHunterX)

---

### Available translations / Доступні переклади / Доступные переводы

- 🇺🇦 [Українська версія](./README_ua.md)
- 🇷🇺 [Русская Версия](./README_ru.md)
- 🇬🇧 English (current)

---
