# Basic structure for django project with docker

A basic structure for working with django and docker

For this model it is necessary:
  - [x] Docker
  - [x] Docker-compose
  - [x] Django (knowledge)

---
 ### How install docker: https://docs.docker.com/engine/install/

 ### How install docker-compose: https://docs.docker.com/compose/install/
 
 ### For knowledge of Django, see the official documentation.
---

## Commands to run the project

When cloning the project, you will have a docker container ready to run on your local machine, but you will have to start for the docker to download the necessary dependencies. Then run to start your container:

```bash
docker-compose up
```
After that, your django container is running, go to "localhost: 8000" and you will see the django page.

The /core folder is the project, of the command "django-admin startproject core ."

## Useful Commands for Managing Django Projects

after running (docker-compose up) in your terminal, open another terminal in the root of the project and run:

Makemigrations:
```bash
docker-compose exec web python manage.py makemigrations
```

still in another terminal, don't forget, another terminal!

Migrate:
```bash
docker-compose exec web python manage.py migrate
```

Create a superuser:
```bash
docker-compose exec web python manage.py createsuperuser
```

Create a app:
```bash
docker-compose exec web django-admin startapp <name_your_app_here>
```

The commands follow the same pattern as django, the way we run it changes only the beginning "docker-compose exec web"

## Useful commands for managing your docker container

To check the status of running containers:
```bash
docker-compose ps
```

To stop containers:
```bash
docker-compose stop
```

To restart containers:
```bash
docker-compose restart
```
---

Soon a template based on this one with mysql connection and also postgree
