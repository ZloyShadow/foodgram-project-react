# Проект Foodgram
![workflow](https://github.com/ZloyShadow/foodgram-project-react/actions/workflows/foodgram_workflow.yml/badge.svg)

[![Python](https://img.shields.io/badge/-Python-464646?style=flat-square&logo=Python)](https://www.python.org/)
[![Django](https://img.shields.io/badge/-Django-464646?style=flat-square&logo=Django)](https://www.djangoproject.com/)
[![Django REST Framework](https://img.shields.io/badge/-Django%20REST%20Framework-464646?style=flat-square&logo=Django%20REST%20Framework)](https://www.django-rest-framework.org/)
[![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-464646?style=flat-square&logo=PostgreSQL)](https://www.postgresql.org/)
[![Nginx](https://img.shields.io/badge/-NGINX-464646?style=flat-square&logo=NGINX)](https://nginx.org/ru/)
[![gunicorn](https://img.shields.io/badge/-gunicorn-464646?style=flat-square&logo=gunicorn)](https://gunicorn.org/)
[![docker](https://img.shields.io/badge/-Docker-464646?style=flat-square&logo=docker)](https://www.docker.com/)
[![GitHub%20Actions](https://img.shields.io/badge/-GitHub%20Actions-464646?style=flat-square&logo=GitHub%20actions)](https://github.com/features/actions)
[![Yandex.Cloud](https://img.shields.io/badge/-Yandex.Cloud-464646?style=flat-square&logo=Yandex.Cloud)](https://cloud.yandex.ru/)

Проект Foodgram позволяет пользователям публиковать рецепты, добавлять рецепты в избранное и список покупок, 
подписыватся на других пользователей и скачивать список продуктов.

Используемые технологии:
Python 3.7
Nginx
React
Docker
Docker-Compose

## Для начала

Сначала склонируйте репозиторий и перейдите в папку.
```
git clone https://github.com/ZloyShadow/foodgram-project-react.git && cd foodgram-project-react/
```

### Требования к программному обеспечению

Для работы с проектом при помощи контейнеров должен быть установлен Docker и docker-compose.


### Запуск приложения

1. Необходимо запустить сборку контейнеров
```
cd infra/ && docker-compose up -d --build
```
2. Необходимо выполнить миграции и собрать статику приложения, для этого запустите скрипт
```
docker exec -ti web python manage.py migrate
```
3. Для использования панели администратора по адресу http://localhost/admin/ необходимо создать суперпользователя.
```
docker exec -it web python manage.py createsuperuser
```

Проект запущен и доступен по [адресу](http://158.160.21.82/)

### Автор: Валентин Ефремов.