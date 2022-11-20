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

## Для запуска проекта

Адрес: http://84.252.129.10

Тестовый суперпользователь:

login: admin@mail.ru password: admin

## Для запуска проекта
- необходимо установить Docker:
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


## Автор проекта
_Ильшат Кушманбетов_, [тут](https://spb.hh.ru/resume/35294e4eff0b572abb0039ed1f6c586556346c) можно посмотреть мое резюме.
