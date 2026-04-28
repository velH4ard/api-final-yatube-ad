# API для Yatube

REST API для социальной сети Yatube.

## Описание

Проект предоставляет API для работы с публикациями, комментариями, сообществами и подписками.

## Возможности

- Публикации (создание, просмотр, редактирование, удаление)
- Комментарии к публикациям
- Сообщества
- Подписки на авторов
- JWT-аутентификация

## Установка

```bash
git clone https://github.com/velH4ard/api-final-yatube-ad.git
cd api-final-yatube-ad
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cd yatube_api
python manage.py migrate
python manage.py runserver
```

## Примеры запросов

### Получение токена

```bash
POST /api/v1/jwt/create/
{
    "username": "user",
    "password": "password"
}
```

### Создание публикации

```bash
POST /api/v1/posts/
{
    "text": "Текст публикации"
}
```

### Подписка на автора

```bash
POST /api/v1/follow/
{
    "following": "username"
}
```
