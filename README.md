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

At this step bare webapp is ready:
http://localhost:8000/

Setting up backpack:

    ./artisan migrate
    ./artisan db:seed --class="Backpack\Settings\database\seeds\SettingsTableSeeder"
    ./artisan db:seed

Open http://localhost:8000/admin

Done.

