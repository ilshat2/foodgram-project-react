# Foodgram

## Cервис для публикаций и обмена рецептами 

### Структура проекта:
```
ilshat2
 └── foodgram-project-react
     ├── .gihub/workflows
     ├── backend  <-- бэкенд продуктового помощника
     |   ├── Dockerfile
     |   ├── manage.py
     |   ├── requirements.txt
     |   ├── setup.cfg
     |   └── backend
     |       ├── __init__.py 
     |       ├── asgi.py
     |       ├── Dockerfile
     |       ├── settings.py
     |       ├── urls.py
     |       └── wsgi.py
     ├── data <-- список ингредиентов с единицами измерения.
     ├── docs <-- файлы спецификации API.
     ├── frontend <-- файлы, необходимые для сборки фронтенда приложения.
     ├── infra <-- инфраструктура проекта: конфигурационный файл nginx и docker-compose.yml.
     ├── .gitignore
     ├── README.md 
     ├── requirements.txt
     └── setup.cfg
```

## Инфраструктура

- Проект работает с СУБД PostgreSQL.
- Проект запущен на сервере в Яндекс.Облаке в трёх контейнерах: nginx, PostgreSQL и Django+Gunicorn. Контейнер с проектом обновляется на Docker Hub
- В nginx настроена раздача статики, остальные запросы переадресуются в Gunicorn.
- Данные сохраняются в volumes.
- Код соответствует PEP8.


## Для запуска проекта необходимо
- установить Docker:
```
https://docs.docker.com/engine/install/
```
- клонировать репозиторий к себе на сервер командой:
```
https://github.com/ilshat2/foodgram-project-react
```
- перейдити в каталок проекта:
```
cd foodgram-project-react
```
- создайть файл окружений
```
touch.env
```
- и заполнить его:
```
DB_NAME=postgres # имя базы postgres
POSTGRES_USER=postgres # имя пользователя postgres 
POSTGRES_PASSWORD=postgres # пароль для базы postgres 
DB_HOST=db #имя хоста базы данных 
DB_PORT=5432 #порт
```
- перейдити в каталог infra и запустите создание контейнеров:
```
docker-compose up -d --build
```
- первоначальная настройка проекта:
```
docker-compose exec backend python manage.py migrate --noinput
```
- создание суперпользователя:
```
docker-compose exec backend python manage.py collectstatic --no-input
```
- загрузка фикстур:
```
docker-compose exec backend python manage.py createsuperuser
```
После сборки, проект будет доступен по имени хоста вашей машины, на которой был развернут проект.


Адрес: http://

Тестовый суперпользователь:

login: admin@mail.ru password: admin

## Автор проекта
_Ильшат Кушманбетов_, [тут](https://spb.hh.ru/resume/35294e4eff0b572abb0039ed1f6c586556346c) можно посмотреть мое резюме.
