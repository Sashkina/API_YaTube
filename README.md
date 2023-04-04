# api_final

### Описание:

*YaTube - это социальная сеть.
Она дает пользователям возможность создать учетную запись, публиковать записи, подписываться на любимых авторов и комментировать понравившиеся записи.
REST API для Yatube - это интерфейс, через который смогут работать мобильное приложение или чат-бот; через него же можно будет передавать данные в любое приложение или на фронтенд.*


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

**Request sample:**
POST /api/v1/posts/

{
"text": "string",
"image": "string",
"group": 0
}

**Response sample:**
{
"id": 0,
"author": "string",
"text": "string",
"pub_date": "2019-08-24T14:15:22Z",
"image": "string",
"group": 0
}

2. **Получение комментариев**

**Request sample:**
GET /api/v1/posts/{post_id}/comments/

**Response sample:**
[
{
"id": 0,
"author": "string",
"text": "string",
"created": "2019-08-24T14:15:22Z",
"post": 0
}
]
