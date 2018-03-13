1. Install Docker: https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-docker-ce-1
2. Install docker-compose: https://docs.docker.com/compose/install/#prerequisites
3. Run:

```
docker-compose build
docker volume create --name=iatidata
docker-compose up #Followed by CTRL+BREAK
docker-compose run web python manage.py migrate
docker-compose run web python manage.py createsuperuser
docker-compose run web python manage.py collectstatic --noinput
docker-compose up
```