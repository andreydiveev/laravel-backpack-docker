# Installation:

Install docker:

    curl https://releases.rancher.com/install-docker/17.12.sh | sh

Install docker-ompose:

    curl -L --fail https://github.com/docker/compose/releases/download/1.12.0/run.sh > /usr/local/bin/docker-compose
    chmod +x /usr/local/bin/docker-compose
    docker-compose --version

Install app:

    git clone https://github.com/andreydiveev/laravel-backpack-docker
    cd laravel-backpack-docker
    docker-compose up -d

wait for composer install the project, see it by:

    docker-compose logs -f composer

next:

    docker-compose exec php bash
    cp .env.example .env
    php artisan key:generate

At this step bare webapp is ready:
http://localhost/

Setting up backpack:

    php artisan migrate
    php artisan db:seed --class="Backpack\Settings\database\seeds\SettingsTableSeeder"
    php artisan db:seed

Open http://localhost/admin

Done.

