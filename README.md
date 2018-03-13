```
docker-compose build
docker volume create --name=iatidata
docker-compose up #Followed by CTRL+BREAK
docker-compose run web python manage.py migrate
docker-compose run web python manage.py createsuperuser
docker-compose run web python manage.py collectstatic --noinput
docker-compose up
```