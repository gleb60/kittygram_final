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
### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/yandex-praktikum/kittygram_backend.git
```

```
cd kittygram_final/kittygram_backend
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

* Если у вас Linux/macOS

    ```
    source env/bin/activate
    ```

* Если у вас windows

    ```
    source env/scripts/activate
    ```

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

