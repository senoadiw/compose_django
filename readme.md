Django+PostgreSQL Development With Docker

Based on https://docs.docker.com/compose/django/

First start:

* git clone https://github.com/senoadiw/compose_django.git
* cd compose_django
* docker-compose build
* docker-compose up -d
* docker-compose ps
* docker exec -it composedjango_web_1 bash
    * python manage.py migrate
    * python manage.py createsuperuser
    * exit
* docker-machine ip default
* Open http://dockermachineip:8000

Subsequent starts:

* docker-compose up -d
* docker-compose ps
* docker-machine ip default
* docker exec -it composedjango_web_1 bash
* Open http://dockermachineip:8000
