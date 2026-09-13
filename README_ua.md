# <img src="PNG/CreepyEYE_mini_baner.png" style="height: 100px !important;width: 300px !important;" ></a>

![License: MIT](https://img.shields.io/badge/License-MIT-purple) 
![Status: Stable](https://img.shields.io/badge/Status-Stable-green) 
![Version: 1.2](https://img.shields.io/badge/Version-1.2-darkred.svg)
![Python 3.8+](https://img.shields.io/badge/Python-3.8%2B-blue) 
![OS: Windows/Linux/Mac](https://img.shields.io/badge/OS-Windows%20|%20Linux%20|%20Mac-lightgrey)
![Last Commit](https://img.shields.io/github/last-commit/CreepyHunterX/CreepyEYE-Genesis.svg)
![Open Issues](https://img.shields.io/github/issues/CreepyHunterX/CreepyEYE-Genesis.svg)
&nbsp;

## ⚠️ ВАЖЛИВО!
**CreepyEYE Genesis** — OSINT-інструмент (Open Source Intelligence) для пошуку за username, email, IP, доменом і номером телефону.  
**Використовуйте тільки в етичних цілях! Розробники не несуть відповідальності за ваші дії.**

---

| Windows | Linux |
|---------|-------|
| <img src="./PNG/CE_Windows_ua.png" alt="CreepyEYE Genesis - Ukrainian UI on Windows" width="340"> | <img src="./PNG/CE_Linux_ua.png" alt="CreepyEYE Genesis - Ukrainian UI on Linux" width="340"> |




## 🛠️ Можливості

🔎 Пошук username:  
&nbsp;&nbsp;&nbsp;&nbsp;`GitHub`, `X`, `Instagram`, `TikTok`, `Facebook`, `GitLab`, `Bitbucket`, `Reddit`, `Twitch`, `Kaggle`, `Medium`, `SoundCloud`, `Spotify`

📧 Перевірка email:  
&nbsp;&nbsp;&nbsp;&nbsp;через `Hunter.io`, `EmailRep.io`  
🌐 IP/домен перевірка:  
&nbsp;&nbsp;&nbsp;&nbsp;через `IPinfo`, `Shodan`, `AbuseIPDB`, `VirusTotal`, `GreyNoise`, `Whois`  
📱 Телефонні номери: `Numverify`  
🧅 Маршрутизація запитів через Tor  
🈯 Меню з вибором мови (`Українська` / `Англійська` / `Російська`)  
🧾 Сирий JSON-вивід (пункт меню `9`, без перезапуску)  
💾 Збереження результатів скану в JSON у теку `reports/`  
⚙️ Автоматичне встановлення залежностей

---

## Скріншоти (UA / RU / EN)

| Мова | Windows | Linux |
|----------|---------|-------|
| Українська | <img src="./PNG/CE_Windows_ua.png" alt="CreepyEYE Genesis - Ukrainian UI on Windows" width="340"> | <img src="./PNG/CE_Linux_ua.png" alt="CreepyEYE Genesis - Ukrainian UI on Linux" width="340"> |
| Російська | <img src="./PNG/CE_Windows_ru.png" alt="CreepyEYE Genesis - Russian UI on Windows" width="340"> | <img src="./PNG/CE_Linux_ru.png" alt="CreepyEYE Genesis - Russian UI on Linux" width="340"> |
| Англійська | <img src="./PNG/CE_Windows.png" alt="CreepyEYE Genesis - English UI on Windows" width="340"> | <img src="./PNG/CE_Linux.png" alt="CreepyEYE Genesis - English UI on Linux" width="340"> |

---

## Встановлення

1. **Встановіть Python 3.8+**  
   [Завантажити Python](https://www.python.org/downloads/)

2. **Встановіть Git**  
   - Windows: [Завантажити Git](https://git-scm.com/downloads/win)
   - Linux: `sudo apt update && sudo apt install git`
   - MacOS: [Завантажити Git](https://git-scm.com/downloads/mac)

3. **Склонуйте репозиторій**  
   ```sh
   git clone https://github.com/CreepyHunterX/CreepyEYE-Genesis.git
   cd "CreepyEYE-Genesis"
   ```

4. **Встановіть залежності**  
   ```sh
   pip install -r requirements.txt
   ```

5. **Запустіть програму**  
   ```sh
   python ce_genesis.py
   ```

6. **Запустіть тести** *(необов'язково, для контриб'юторів)*  
   ```sh
   python -m unittest discover -s tests
   ```

---

## Налаштування API ключів

API ключі зберігаються у файлі `settings/api/api_keys.env`.  
Для редагування ключів використовуйте **`6. Налаштування API`**. CreepyEYE створює `api_keys.env` із шаблону, якщо його немає, відкриває в редакторі за замовчуванням і після цього просить перезапуск, щоб завантажити нові ключі. Файл також можна редагувати вручну.  
Значення-заглушки (`your_shodan_api_key`, …) вважаються незаданими. Підтримувані змінні:

- SHODAN_API_KEY
- IPINFO_TOKEN
- ABUSEIPDB_KEY
- HUNTER_API_KEY
- VIRUSTOTAL_API_KEY
- NUMVERIFY_API_KEY
- GREYNOISE_API_KEY
- EMAILREP_API_KEY
- WHOIS_API_KEY

### Де взяти ключі

| Сервіс        | URL для ключа                             | Призначення                                     |
|---------------|-------------------------------------------|------------------------------------------------|
| Shodan        | https://www.shodan.io/                    | Сканування IP, пристроїв, відкритих портів     |
| IPinfo        | https://ipinfo.io/                        | Геолокація IP та інформація про ASN            |
| AbuseIPDB     | https://www.abuseipdb.com/                | Перевірка, чи повідомляли про зловмисну активність IP |
| Hunter.io     | https://hunter.io/                        | Перевірка email та пошук по домену            |
| Numverify     | https://numverify.com/                     | Валідація телефонних номерів                   |
| GreyNoise     | https://greynoise.io/                 | Інформація про сканери та ботів в мережі      |
| EmailRep.io   | https://emailrep.io/                       | Перевірка репутації email адрес                |
| WhoisXML API  | https://whoisxmlapi.com/                  | Дані WHOIS та інформація про домени            |
| VirusTotal    | https://www.virustotal.com/               | Перевірка IP, доменів та файлів на шкідливе ПЗ |


---

## Tor

Запустіть Tor Browser або tor.exe перед запуском CreepyEYE. Якщо Tor доступний, запити йдуть через нього.

---

## JSON-вивід

Пункт меню **`9`** перемикає сирий JSON-вивід (`JSON-вивід: УВІМК / ВИМК`). Коли увімкнено, кожен модуль додатково виводить необроблену відповідь API. Корисно для налагодження та передачі відповідей модулів іншим інструментам. Діє одразу й не впливає на збережені звіти.

---

## Звіти

Після кожного скану CreepyEYE питає `Зберегти повний звіт? (y/n)`. При `y` звіт записується в:

```
reports/<ціль>_<тип>_<РРРРММДД-ГГХВСС>.json
```

UTF-8 JSON з версією інструменту, ціллю та її типом, часом початку й завершення (UTC), ознакою того, чи запити реально йшли через Tor, і результатами кожного модуля. API ключі вирізаються перед записом.

> ⚠️ `reports/` у `.gitignore`: звіти містять дані про ціль. Не комітьте їх і не прикріплюйте до issues/PR.

---

## Відмова від відповідальності

Тільки для етичного OSINT. Використовуйте в межах закону.

---

## Ліцензія

[MIT License](LICENSE)

---

## 🧠 CreepyEYE PRO

**CreepyEYE PRO** — платна десктопна редакція для **Windows і Linux** з **довічною ліцензією**. 37 інтеграцій (власні API-ключі); пошук за email, username, доменом, телефоном, IP, імʼям та EXIF фото; експорт звітів; підтримка проксі й Tor. До 3 пристроїв на ключ.

📖 Документація (встановлення, активація, список сервісів, довідка CLI): **[github.com/CreepyCORE/CreepyEYE-PRO](https://github.com/CreepyCORE/CreepyEYE-PRO)**

🛒 **Магазин: [creepycore.com](https://creepycore.com/store)**

> ℹ️ У PRO закритий код. Цей репозиторій — безкоштовна open-source редакція **CreepyEYE Genesis**.

---

## 💸 Підтримати CreepyEYE

Донати йдуть на нові API-інтеграції, роботу над інтерфейсом і швидкодією та регулярні оновлення.

### ☕ Ko-fi
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/F1F71KKMAH)

### 💛 Buy Me a Coffee
[<a href="https://www.buymeacoffee.com/CreepyHunterX" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>](https://buymeacoffee.com/CreepyHunterX)

---

### Доступні переклади / Available translations / Доступные переводы

- 🇺🇦 Українська (поточна)
- 🇷🇺 [Русская Версия](./README_ru.md)
- 🇬🇧 [English Version](./README.md)

---
