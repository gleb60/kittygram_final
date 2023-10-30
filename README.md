# Kittygram

![Actions Status](https://github.com/gleb60/kittygram_final/actions/workflows/main.yml/badge.svg)

## Короткое описание проекта

При любом изменении проекта и пуше его на Гит он автоматически проверяется с помощью Github Actions и при
успешном прохождении тестов он пушится на удаленный сервер и там обновляются все файлы контейнеров, перезапускается
докер и приложение дальше функионирует на удаленном сервере.
Возможности пользователя:

- Зарегистрироваться и авторизоваться
- Добавить нового котика или изменить существующего
- Удалить котика
- Добавить ачивки для питомцев и привязать их к ним
- Смотреть котиков других пользователей

## Технологии

- Приложение запущено на удаленном сервере Яндекса
- Django 3.2.3
- Python 3.9
- Djoser 2.1.0
- PostgreSQL
- Docker
- GitHub Actions
- Gunicorn
- Nginx
- JavaScript (JS)
- Node.js

### Запуск проекта:
1. Клонируйте проект:
```commandline
git@github.com:gleb60/kittygram_final.git
```
2. Скопируйте файлы с локального компьютера на сервер:
```
scp docker-compose.yml <username>@<host>:/home/<username>/
scp nginx.conf <username>@<host>:/home/<username>/
scp .env <username>@<host>:/home/<username>/
пример .env файла находится в корне проекта и называется .env.example
```
3. Установите docker и docker-compose:
```
sudo apt install docker.io 
sudo apt install docker-compose
```
4. Соберите контейнер, выполните миграции, создайте суперюзера и соберите статику:
```
sudo docker-compose up -d --build
sudo docker-compose migrate
sudo docker-compose exec backend python manage.py createsuperuser
```
