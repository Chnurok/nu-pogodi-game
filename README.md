# Ну, погоди! — Telegram Mini App

Классическая советская электронная игра в формате Telegram Web App.

## Игра

🐺 **Волк ловит яйца** из 4 гнёзд (верх-лево, верх-право, низ-лево, низ-право)

- **Управление:** касание по углам экрана или клавиши Q/W/A/S
- **Цель:** поймать как можно больше яиц, не уронив 3
- **Прогрессия:** каждые 10 очков скорость увеличивается

## Технологии

- HTML5 Canvas
- Vanilla JavaScript (без фреймворков)
- Telegram WebApp SDK
- Responsive design (мобильные + десктоп)

## Установка

Просто откройте `index.html` в браузере или разверните на любом веб-сервере:

```bash
# Nginx
server {
    listen 8090;
    root /path/to/tg-app;
    index index.html;
}
```

## Интеграция с Telegram Bot

```python
from telegram import InlineKeyboardButton, InlineKeyboardMarkup, WebAppInfo

keyboard = [[InlineKeyboardButton(
    "🥚 Играть", 
    web_app=WebAppInfo(url="https://yourdomain.com/")
)]]
```

## Демо

Запустите локально:
```bash
python3 -m http.server 8090
```

Откройте: http://localhost:8090

## Лицензия

MIT
