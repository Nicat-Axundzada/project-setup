docker-compose run --rm app sh -c 'django-admin startproject app .'
docker-compose build
docker-compose up
docker-compose up --build
docker-compose up -d --build
