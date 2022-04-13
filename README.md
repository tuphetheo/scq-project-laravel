# Source-Code Quality project
This project is for a 3iL course in source-code quality.  
This is a minimalist blog in Laravel and PHP 8.1.

## Requirements
You will need Docker for this project, and a Linux distribution (for Windows only).  
For more info on Linux distributions on Windows, via WSL, see [here](https://docs.microsoft.com/fr-fr/windows/wsl/install).

## Installation
1. Clone the repository
    ```bash
    git clone https://github.com/tuphetheo/scq-project-laravel.git
    ```
   
2. Create the environment variables file, you can change the values to your needs after:
    ```bash
    cp .env.example .env
    ```
   
3. Install dependencies with a Composer image:
    ```bash
    docker run --rm --interactive --tty \
    --volume $PWD:/app \
    composer install
    ```
   
4. Launch the project:
    ```bash
    vendor/bin/sail up -d
    ```
   
5. Generate the application key:
    ```bash
    vendor/bin/sail artisan key:generate 
    ```
   
6. Run the migrations:
    ```bash
    vendor/bin/sail artisan migrate  
    ```
   
7. Install node dependencies and front-end dependencies:
    ```bash
    vendor/bin/sail npm install && vendor/bin/sail npm run dev
    ```
   
You can now access the application at [http://localhost](http://localhost), the dashboard is accessible at [http://localhost/home](http://localhost/home).

## Ressources and original courses
- [Laravel Documentation](https://laravel.com/docs)
- [Blog creation course](https://github.com/nicolas-sanch/creer-minimalist-blog.git) by [Nicolas Sanch](https://github.com/nicolas-sanch)
- [Static Analysis course](https://github.com/nicolas-sanch/static-analysis) by [Nicolas Sanch](https://github.com/nicolas-sanch)
- [SonarCloud Project](https://sonarcloud.io/project/overview?id=tuphetheo_scq-project-laravel)
