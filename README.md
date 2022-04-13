# Minimalist blog using Laravel

## Download and build the project

```bash
git clone https://gitlab.com/tuphetheo/scq-project-laravel.git
cd scq-project-laravel
cp .env.example .env
docker run --rm --interactive --tty \
  --volume $PWD:/app \
  composer install
  
vendor/bin/sail up -d
vendor/bin/sail artisan key:generate               
vendor/bin/sail artisan migrate  
```
