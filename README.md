# Basic structure for django project with docker

A basic structure for working with django and docker

---
 How install docker: https://docs.docker.com/engine/install/
--
 How install docker-compose: https://docs.docker.com/compose/install/
---

## - commands to run the project

Quando clonar o projeto, terá um container docker em mãos pronto para rodar na sua maquina local,
mas vai ter que baixar as dependencias. Então rode para começar o seu container:

```bash
docker-compose up
```

## - comandos utéis para gerenciar projetos do django

Depois que rodar (docker-compose up) em um terminal, abra outro dentro da raiz do projeto e rode:

Para fazer migração:
```bash
docker-compose exec web python manage.py makemigrations
```

Ainda em outro terminal

Para fazer migração pt2:
```bash
docker-compose exec web python manage.py migrate
```

Para criar um superuser:
```bash
docker-compose exec web python manage.py createsuperuser
```

Para criar uma app:
```bash
docker-compose exec web django-admin startapp <nome da app>
```

Os comandos seguem o mesmo padrão do django normal, a diferença é que rodamos com "docker-compose exec"

## - comandos utéis para gerenciar containers docker

Para verificar status dos containers em execução:
```bash
docker-compose ps
```

Para parar os containers:
```bash
docker-compose stop
```

Para reinicar os containers:
```bash
docker-compose restart
```

Para reinicar os containers:
```bash
docker-compose restart
```






