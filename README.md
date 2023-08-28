# API_YaTube

### Описание:

*YaTube - это социальная сеть, которая дает пользователям возможность создать учетную запись,  
публиковать блоги, подписываться на любимых авторов, отмечать  и комментировать  
понравившиеся записи.  
Неавторизованный пользователь может просматривать записи на главной, записи по тегу сообщества, записи конкретного автора.  
REST API для Yatube - это интерфейс, через который смогут работать мобильное приложение или чат-бот;  
через него же можно будет передавать данные в любое приложение или на фронтенд.*

### Технологии:
<li> Python 3.9
<li> Django 3.2.16
<li> djangorestframework 3.12.4

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/Sashkina/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv venv
```

```
source venv/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```

### Примеры:

1. **Создание публикации**

***Request sample:***
POST /api/v1/posts/

```json
{
  "text": "string",
  "image": "string",
  "group": 0
}
```

***Response sample:***
```json
{
  "id": 0,
  "author": "string",
  "text": "string",
  "pub_date": "2019-08-24T14:15:22Z",
  "image": "string",
  "group": 0
}
```

2. **Получение комментариев**

***Request sample:***
GET /api/v1/posts/{post_id}/comments/

***Response sample:***
```json
[
  {
    "id": 0,
    "author": "string",
    "text": "string",
    "created": "2019-08-24T14:15:22Z",
    "post": 0
  }
]
```

### Автор  
Сашкина Кристина
