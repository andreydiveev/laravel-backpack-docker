# Installation:

    git clone https://github.com/andreydiveev/laravel-backpack-docker
    cd laravel-backpack-docker
    docker-compose up -d

wait for composer install the project, see it by:

    docker-compose logs -f composer

next:

    docker-compose exec php bash
    cp .env.example .env
    ./artisan key:generate

