# <img src="PNG/CreepyEYE_mini_baner.png" style="height: 100px !important;width: 300px !important;" ></a>

![License: MIT](https://img.shields.io/badge/License-MIT-purple) 
![Status: Stable](https://img.shields.io/badge/Status-Stable-green) 
![Version: 1.2](https://img.shields.io/badge/Version-1.2-darkred.svg)
![Python 3.8+](https://img.shields.io/badge/Python-3.8%2B-blue) 
![OS: Windows/Linux/Mac](https://img.shields.io/badge/OS-Windows%20|%20Linux%20|%20Mac-lightgrey)
![Last Commit](https://img.shields.io/github/last-commit/CreepyHunterX/CreepyEYE-Genesis.svg)
![Open Issues](https://img.shields.io/github/issues/CreepyHunterX/CreepyEYE-Genesis.svg)
&nbsp;


## ⚠️ ВАЖНО!
**CreepyEYE Genesis** — OSINT-инструмент (Open Source Intelligence) для поиска по username, email, IP, домену и номеру телефона.  
**Используйте только в этических целях! Разработчики не несут ответственности за ваши действия.**

⚠️ Русский перевод поддерживается сообществом. Официальные языки — английский и украинский; за точность перевода авторы не отвечают.

---

| Windows | Linux |
|---------|-------|
| <img src="./PNG/CE_Windows_ru.png" alt="CreepyEYE Genesis - Russian UI on Windows" width="340"> | <img src="./PNG/CE_Linux_ru.png" alt="CreepyEYE Genesis - Russian UI on Linux" width="340"> |




## 🛠️ Возможности

🔎 Поиск username:  
&nbsp;&nbsp;&nbsp;&nbsp;`GitHub`, `X`, `Instagram`, `TikTok`, `Facebook`, `GitLab`, `Bitbucket`, `Reddit`, `Twitch`, `Kaggle`, `Medium`, `SoundCloud`, `Spotify`

📧 Проверка email:  
&nbsp;&nbsp;&nbsp;&nbsp;через `Hunter.io`, `EmailRep.io`  
🌐 Проверка IP/доменов:  
&nbsp;&nbsp;&nbsp;&nbsp;через `IPinfo`, `Shodan`, `AbuseIPDB`, `VirusTotal`, `GreyNoise`, `Whois`  
📱 Телефоны: `Numverify`  
🧅 Маршрутизация запросов через Tor  
🈯 Меню выбора языка (`Украинский` / `Английский` / `Русский`)  
🧾 Сырой JSON-вывод (пункт меню `9`, без перезапуска)  
💾 Сохранение результатов скана в JSON в папку `reports/`  
⚙️ Автоматическая установка зависимостей

---

## Скриншоты (RU / UA / EN)

| Язык | Windows | Linux |
|----------|---------|-------|
| Русский  | <img src="./PNG/CE_Windows_ru.png" alt="CreepyEYE Genesis - Russian UI on Windows" width="340"> | <img src="./PNG/CE_Linux_ru.png" alt="CreepyEYE Genesis - Russian UI on Linux" width="340"> |
| Украинский | <img src="./PNG/CE_Windows_ua.png" alt="CreepyEYE Genesis - Ukrainian UI on Windows" width="340"> | <img src="./PNG/CE_Linux_ua.png" alt="CreepyEYE Genesis - Ukrainian UI on Linux" width="340"> |
| Английский | <img src="./PNG/CE_Windows.png" alt="CreepyEYE Genesis - English UI on Windows" width="340"> | <img src="./PNG/CE_Linux.png" alt="CreepyEYE Genesis - English UI on Linux" width="340"> |

---

## Установка

1. **Установите Python 3.8+**  
   [Скачать Python](https://www.python.org/downloads/)

2. **Установите Git**  
   - Windows: [Скачать Git](https://git-scm.com/downloads/win)  
   - Linux: `sudo apt update && sudo apt install git`  
   - MacOS: [Скачать Git](https://git-scm.com/downloads/mac)

3. **Клонируйте репозиторий**  
   ```sh
   git clone https://github.com/CreepyHunterX/CreepyEYE-Genesis.git
   cd "CreepyEYE-Genesis"
   ```

4. **Установите зависимости**

   ```sh
   pip install -r requirements.txt
   ```

5. **Запуск программы**

   ```sh
   python ce_genesis.py
   ```

6. **Запуск тестов** *(необязательно, для контрибьюторов)*

   ```sh
   python -m unittest discover -s tests
   ```

---

## Настройка API ключей

API ключи хранятся в файле `settings/api/api_keys.env`.  
Для редактирования ключей используйте **`6. Настройки API`**. CreepyEYE создаёт `api_keys.env` из шаблона, если его нет, открывает в редакторе по умолчанию и затем запрашивает перезапуск для загрузки новых ключей. Файл также можно редактировать вручную.  
Значения-заглушки (`your_shodan_api_key`, …) считаются незаданными. Поддерживаемые переменные:

* SHODAN\_API\_KEY
* IPINFO\_TOKEN
* ABUSEIPDB\_KEY
* HUNTER\_API\_KEY
* VIRUSTOTAL\_API\_KEY
* NUMVERIFY\_API\_KEY
* GREYNOISE\_API\_KEY
* EMAILREP\_API\_KEY
* WHOIS\_API\_KEY

### Где взять ключи

| Сервис       | Ссылка на API                                              | Назначение                                               |
| ------------ | ---------------------------------------------------------- | -------------------------------------------------------- |
| Shodan       | [https://www.shodan.io/](https://www.shodan.io/)           | Сканирование IP, устройств, открытых портов              |
| IPinfo       | [https://ipinfo.io/](https://ipinfo.io/)                   | Геолокация IP и ASN                                      |
| AbuseIPDB    | [https://www.abuseipdb.com/](https://www.abuseipdb.com/)   | Проверка, не сообщалось ли о вредоносной активности с IP |
| Hunter.io    | [https://hunter.io/](https://hunter.io/)                   | Проверка email и поиск по домену                         |
| Numverify    | [https://numverify.com/](https://numverify.com/)           | Проверка номеров телефонов                               |
| GreyNoise    | [https://greynoise.io/](https://greynoise.io/)     | Контекст сканеров/ботов                                  |
| EmailRep.io  | [https://emailrep.io/](https://emailrep.io/)               | Репутация email адресов                                  |
| WhoisXML API | [https://whoisxmlapi.com/](https://whoisxmlapi.com/)       | WHOIS данные и информация о доменах                      |
| VirusTotal   | [https://www.virustotal.com/](https://www.virustotal.com/) | Сканирование IP, доменов и файлов на вирусы              |

---

## Tor

Запустите Tor Browser или tor.exe перед запуском CreepyEYE. Если Tor доступен, запросы идут через него.

---

## JSON-вывод

Пункт меню **`9`** переключает сырой JSON-вывод (`JSON-вывод: ВКЛ / ВЫКЛ`). Когда включено, каждый модуль дополнительно выводит необработанный ответ API. Полезно для отладки и передачи ответов модулей другим инструментам. Действует сразу и не влияет на сохранённые отчёты.

---

## Отчёты

После каждого скана CreepyEYE спрашивает `Сохранить полный отчёт? (y/n)`. При `y` отчёт записывается в:

```
reports/<цель>_<тип>_<ГГГГММДД-ЧЧММСС>.json
```

UTF-8 JSON с версией инструмента, целью и её типом, временем начала и завершения (UTC), признаком того, шли ли запросы реально через Tor, и результатами каждого модуля. API ключи вырезаются перед записью.

> ⚠️ `reports/` в `.gitignore`: отчёты содержат данные о цели. Не коммитьте их и не прикрепляйте к issues/PR.

---

## Отказ от ответственности

Только для этичного OSINT. Используйте в рамках закона.

---

## Лицензия

[MIT License](LICENSE)

---

## 🧠 CreepyEYE PRO

**CreepyEYE PRO** — платная десктопная редакция для **Windows и Linux** с **пожизненной лицензией**. 37 интеграций (свои API-ключи); поиск по email, username, домену, телефону, IP, имени и EXIF фото; экспорт отчётов; поддержка прокси и Tor. До 3 устройств на ключ.

📖 Документация (установка, активация, список сервисов, справка CLI): **[github.com/CreepyCORE/CreepyEYE-PRO](https://github.com/CreepyCORE/CreepyEYE-PRO)**

🛒 **Магазин: [creepycore.com](https://creepycore.com/store)**

> ℹ️ У PRO закрытый код. Этот репозиторий — бесплатная open-source редакция **CreepyEYE Genesis**.

---

## 💸 Поддержать CreepyEYE

Донаты идут на новые API-интеграции, работу над интерфейсом и производительностью и регулярные обновления.

### ☕ Ko-fi
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/F1F71KKMAH)

### 💛 Buy Me a Coffee
[<a href="https://www.buymeacoffee.com/CreepyHunterX" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>](https://buymeacoffee.com/CreepyHunterX)

---

### Доступные переводы / Available translations / Доступні переклади 

- 🇺🇦 [Українська версія](./README_ua.md)
- 🇷🇺 Русский (текущий)
- 🇬🇧 [English Version](./README.md)

---
