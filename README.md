# API_FINAL_YATUBE
REST API для проекта Yatube
# Стек технологий
- фреймворк Django
- апи Django REST Framework
- аутентификация Simple JWT
# Установка и запуск
Клонирйте репозиторий
```
git clone https://github.com/podlev/api_final_yatube
```
Установить и активировать виртуальное окружение
```
cd api_final_yatube
python -m venv venv
Source venv/Scripts/activate
```
Установить зависимости
```
python3 -m pip install --upgrade pip
pip install -r requirements.txt
```
Выполнить миграции:
```
cd yatube_ap
python manage.py migrate
```
Запустить проект
```
python manage.py runserver
```
Проект доступен по адресу: 
http://127.0.0.1:8000/
# Документация
После запуска сервера документация будет доступна по адресу:
http://127.0.0.1:8000/redoc/