#  Как работать с репозиторием финального задания
![GitHub Action Workflow](https://github.com/kaluginpeter/kittygram_final/actions/workflows/main.yml/badge.svg)
## Что нужно сделать
### About
KittyGram - Social service for people who loves sweety cats(who not loves cats?).
You can register in app, create posts about your animals and pin a photo.
Also you can see pets of another people. Have a fun!
Настроить запуск проекта Kittygram в контейнерах и CI/CD с помощью GitHub Actions
### Stack Technologies
Python/Django/Django Rest/NodeJs/Docker/PostgresSql/GitHub Actions
### Getting Started
1) Pull repo from github
```
git pull git@github.com:kaluginpeter/kittygram_final.git
```
2) Add variables in .env file
3) Launch Dokcer Compose file
```
docker compose up
```
4) Done!
### How to add .env file

POSTGRES_USER=name_user_for_postgres (only for production)

POSTGRES_PASSWORD=password_for_postgres (only for production)

POSTGRES_DB=name_of_db (only for production)

DB_HOST=name_of_postgres_db (for docker network connection) (only for production)

DB_PORT=5432 for connecting Backend Container

SECRET_KEY=project_secret_key

DEVELOPMENT=False boolean (Set to False for production otherwise True)

POSTGRES_DATABASE=True boolean (Set to False for using SQLite)

HOSTS_ALLOWED='localhost' (write a allowed hosts SEPARATED BY SINGE WHITESPACE)

### Author
@kaluginpeter
## Как проверить работу с помощью автотестов

В корне репозитория создайте файл tests.yml со следующим содержимым:
```yaml
repo_owner: ваш_логин_на_гитхабе
kittygram_domain: полная ссылка (https://доменное_имя) на ваш проект Kittygram
taski_domain: полная ссылка (https://доменное_имя) на ваш проект Taski
dockerhub_username: ваш_логин_на_докерхабе
```

Скопируйте содержимое файла `.github/workflows/main.yml` в файл `kittygram_workflow.yml` в корневой директории проекта.

Для локального запуска тестов создайте виртуальное окружение, установите в него зависимости из backend/requirements.txt и запустите в корневой директории проекта `pytest`.

## Чек-лист для проверки перед отправкой задания

- Проект Taski доступен по доменному имени, указанному в `tests.yml`.
- Проект Kittygram доступен по доменному имени, указанному в `tests.yml`.
- Пуш в ветку main запускает тестирование и деплой Kittygram, а после успешного деплоя вам приходит сообщение в телеграм.
- В корне проекта есть файл `kittygram_workflow.yml`.
