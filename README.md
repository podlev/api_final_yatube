# API_FINAL_YATUBE
### Описание
**Учебный проект.** REST API для проекта Yatube - социальной сети позволяющей писать посты, добавлять картинки, оставлять комментарии, подписываться на других авторов.
### Технологии
- Python 3.7
- Django 2
- аутентификация Simple JWT
### Запуск проекта в dev-режиме
- Установите и активируйте виртуальное окружение
- Установите зависимости из файла requirements.txt
```
pip install -r requirements.txt
```
- Перейдите в папку с manage.py
```
cd yatube_api
```
- Выполните миграции
```
python manage.py makemigrations
python manage.py migrate
```
Для зауска dev сервера выполните команду:
```
python3 manage.py runserver
```
### Примеры
- Для доступа к API необходимо получить токен: POST-запрос localhost:8000/api/v1/api-token-auth/ передав поля login и password, в ответе на запрос приходит token (JWT-токен).
```
{ 
    "login": "string",
    "password": "string" 
}
```
- Затем, отправляя токен с каждым запросом, можно будет обращаться к методам, например:
```
api/v1/posts/ (GET, POST): получаем список всех постов или создаём новый пост.
api/v1/posts/{post_id}/ (GET, PUT, PATCH, DELETE): получаем, редактируем или удаляем пост по id.
api/v1/groups/ (GET): получаем список всех групп.
api/v1/groups/{group_id}/ (GET): получаем информацию о группе по id.
api/v1/posts/{post_id}/comments/ (GET, POST): получаем список всех комментариев поста с id=post_id или создаём новый, указав id поста, который хотим прокомментировать.
api/v1/posts/{post_id}/comments/{comment_id}/ (GET, PUT, PATCH, DELETE): получаем, редактируем или удаляем комментарий по id у поста с id=post_id.
```
- При отправке запроса необходимо передать токен в заголовке Authorization: Bearer <токен>
- Основной список ресурсов API http://127.0.0.1:8000/redoc/
