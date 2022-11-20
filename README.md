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
