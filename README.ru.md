<div align="center">

# 🎯 Бот для отслеживания инвайтов в Discord

*Мощный Discord-бот для отслеживания приглашений с настраиваемыми стилями общения*

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)  
[![Discord.py](https://img.shields.io/badge/discord.py-2.3.0+-blue.svg)](https://github.com/Rapptz/discord.py)  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/MrFolium/discord-invite-tracker-bot/blob/main/LICENSE)

[Функции](#-функции) • [Установка](#-установка) • [Команды](#-команды) • [Конфигурация](#-конфигурация) • [Логирование](#-логирование)

</div>

---

## ✨ Функции

<table>
<tr>
<td width="50%">

### 🎯 **Основные возможности**
- 📊 **Отслеживание инвайтов в реальном времени**
- 🎉 **Приветственные сообщения**
- 👋 **Уведомления об уходе**
- 🏆 **Интерактивные лидерборды**
- 📝 **Подробное логирование**

</td>
<td width="50%">

### 🎨 **Настройка**
- 🌍 **Многоязычная поддержка**
- 🎭 **Стили общения**
- ⚙️ **Гибкая конфигурация**
- 🔄 **Горячая перезагрузка настроек**
- 🚀 **Фоновый режим работы**

</td>
</tr>
</table>

---

## 🎨 Стили общения

<div align="center">

| Стиль | Язык | Тон | Описание |
|-------|------|-----|----------|
| 🇷🇺 **casual_ru** | Русский | Дружелюбный | Неформальный стиль общения |
| 🇷🇺 **formal_ru** | Русский | Официальный | Деловой официальный стиль |
| 🇬🇧 **casual_en** | Английский | Дружелюбный | Тёплый приветственный стиль |
| 🇬🇧 **formal_en** | Английский | Официальный | Строгий деловой стиль |

</div>

---

## 🚀 Установка

### Быстрый старт

```bash
# 1. Скачайте проект
git clone https://github.com/MrFolium/discord-invite-tracker-bot.git
cd discord-invite-tracker-bot

# 2. Настройте окружение
cp .env.example .env
# Отредактируйте .env и добавьте токен бота и ID сервера

# 3. Запуск бота
# Windows:
start.bat
# Linux/Mac:
./start.sh
```

### 📋 Требования

- **Python 3.8+**
- **Токен Discord-бота** ([получить здесь](https://discord.com/developers/applications))
- **Права администратора на сервере**

---

## 🎮 Команды

<details>
<summary><b>📊 Основные команды</b></summary>

| Команда | Описание | Пример |
|---------|----------|--------|
| `!invites` | Показать количество инвайтов | `!invites @user` |
| `!leaderboard` | Топ пригласивших | `!leaderboard 10` |
| `!whoinvited` | Кто пригласил участника | `!whoinvited @user` |

</details>

<details>
<summary><b>🎨 Управление стилем</b></summary>

| Команда | Описание | Пример |
|---------|----------|--------|
| `!styles` | Список доступных стилей | `!styles` |
| `!setstyle` | Сменить стиль общения | `!setstyle casual_ru` |

</details>

<details>
<summary><b>⚙️ Админ-команды</b></summary>

| Команда | Описание | Пример |
|---------|----------|--------|
| `!resetinvites` | Сброс инвайтов пользователя | `!resetinvites @user` |
| `!resetall` | Сброс всех инвайтов | `!resetall` |
| `!reloadconfig` | Перезагрузить настройки | `!reloadconfig` |

</details>

---

## 📝 Логирование

- 📁 Автоматическое создание папки логов  
- 📝 Все события записываются в `logs/bot.log`  
- 🚀 Логируются запуск и остановка  
- ❌ Отслеживаются ошибки  
- 👥 Мониторинг активности пользователей

### 📂 Файл логов
```
logs/
└── bot.log
```

---

## ⚙️ Конфигурация

### 📁 Структура проекта

```
discord-invite-bot/
├── main.py                 # Главный файл бота
├── modules/                # Модули
│   ├── config_manager.py
│   └── invite_logger.py
├── config/                 # Настройки
│   ├── config.json
│   └── styles/
│       ├── casual_ru.json
│       ├── formal_ru.json
│       ├── casual_en.json
│       └── formal_en.json
├── start.bat
├── start.sh
├── requirements.txt
├── .env.example
├── data/                   # Создаётся автоматически
├── logs/                   # Логи
│   └── bot.log
└── .env                    # Настройки среды
```

### 🔧 Файл `.env`

```env
DISCORD_TOKEN=ваш_токен
GUILD_ID=ваш_id_сервера
DEBUG=false
LOG_LEVEL=INFO
```

---

## 💡 Примеры использования

```bash
!styles                 # Список стилей
!setstyle casual_ru     # Переключение на русский стиль
!invites                # Проверка инвайтов
!leaderboard 10         # Топ 10
!resetinvites @user     # Сброс инвайтов
!reloadconfig           # Перезагрузка конфигурации
```

---

## 🎭 Примеры стиля

> **Неформальный стиль (русский):**  
> 🎉 Привет, @новичок! Добро пожаловать в наше сообщество!  
> 👤 Пригласил: @пригласивший  
> 📊 У него теперь 5 инвайтов!

> **Официальный стиль (английский):**  
> 🎉 Welcome to the server, @newuser.  
> 👤 Invited by: @inviter  
> 📊 Current invitation count: 5

---

## 🛠️ Решение проблем

<div align="center">

1. ✅ **Бот не отвечает?** — Проверьте файл `.env`  
2. 🔐 **Проблемы с правами?** — Дайте боту права администратора  
3. 📋 **Ошибки при запуске?** — Посмотрите `logs/bot.log`  
4. 🔄 **Команды не работают?** — Попробуйте `!reloadconfig`

[Создать Issue](https://github.com/MrFolium/discord-invite-tracker-bot/issues)

</div>

---

<div align="center">

## 📄 Лицензия

Проект распространяется по лицензии **MIT**

*Сделано с ❤️ для Discord-сообществ*

**[⭐ Поставить звезду](https://github.com/MrFolium/discord-invite-tracker-bot)** • **[🍴 Форк проекта](https://github.com/MrFolium/discord-invite-tracker-bot/fork)** • **[📝 Сообщить об ошибке](https://github.com/MrFolium/discord-invite-tracker-bot/issues)**

</div>
