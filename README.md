# laravel-octane-docker
🚀 Build blazing-fast Laravel Octane apps with this generic 🐋 Docker image

## Usage

Production `Dockerfile`

```Dockerfile
FROM osbre/laravel-octane-docker:latest

ENV APP_ENV=production
ENV APP_DEBUG=false

COPY . .

RUN composer install --no-dev --prefer-dist --no-interaction

EXPOSE 8000

ENTRYPOINT ["php", "artisan", "octane:start", "--host=0.0.0.0", "--port=8000"]
```
