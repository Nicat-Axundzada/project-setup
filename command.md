docker-compose run --rm app sh -c 'django-admin startproject app .'
docker-compose build
docker-compose up
docker-compose up --build
docker-compose up -d --build
docker-compose run --rm app sh -c 'python manage.py startapp utils'
docker-compose run --rm app sh -c 'python manage.py wait_for_db'
