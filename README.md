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

