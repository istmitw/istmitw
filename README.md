docker run -d --name oneindex \
    -p 80:80 --restart=always \
    -v ~/oneindex/config:/var/www/html/config \
    -v ~/oneindex/cache:/var/www/html/cache \
    -e REFRESH_TOKEN='0 * * * *' \
    -e REFRESH_CACHE='*/10 * * * *' \
    setzero/oneindex
