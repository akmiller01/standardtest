```
docker-compose build
docker volume create --name=iatidata
docker-compose up
docker-compose run web python manage.py migrate
docker-compose run web python manage.py createsuperuser
docker-compose run web python manage.py collectstatic --noinput
```