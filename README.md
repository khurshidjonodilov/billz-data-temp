# BILLZ Label Bot

Автоматическое проставление меток в Омнидеске через OpenAI.

## Переменные окружения (Railway)

| Переменная | Значение |
|---|---|
| OPENAI_API_KEY | Ваш ключ OpenAI |
| OMNIDESK_API_KEY | Ваш API ключ Омнидеска |
| OMNIDESK_DOMAIN | billz.omnidesk.ru |

## Деплой на Railway

1. Зарегистрируйтесь на railway.app
2. Создайте новый проект → Deploy from GitHub
3. Загрузите эти файлы в GitHub репозиторий
4. Добавьте переменные окружения в Railway
5. Скопируйте URL вашего сервиса

## Подключение к Омнидеску

В правиле автоматизации добавьте действие:
- HTTP запрос → POST → https://ВАШ_URL.railway.app/webhook
- Body: {"case_id": "[case_id]", "content": "[case_description]"}
