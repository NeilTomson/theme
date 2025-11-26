
docker command:
    Stop all the containers
    docker stop $(docker ps -a -q)
    Remove all the containers
    docker rm $(docker ps -a -q)

use:
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v "$(pwd):/var/www/html" \
    -w /var/www/html \
    laravelsail/php84-composer:latest \
    composer install --ignore-platform-reqs
