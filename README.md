## Cloning Laravel Project from GitHub

Follow these steps to clone and set up a Laravel project from this repository:

1. Clone the repository:
   ```bash
   git clone <GitHub Repository URL>
   ```

2. Navigate to the cloned repository using your Command Prompt (CMD) or Terminal:
   ```bash
   cd <Cloned project name>
   ```

3. Install project dependencies using Composer:
   ```bash
   composer install
   ```

4. If you encounter any errors, they may be due to obsolete or deprecated packages. Run this command to update the dependencies:
   ```bash
   composer update
   ```

5. Copy the example environment file:
   ```bash
   cp .env.example .env
   ```

6. If you encounter an error with the 'cp' command, you can use this command instead:
   ```bash
   copy .env.example .env
   ```

7. Open your .env file and adjust the database name (DB_DATABASE), username (DB_USERNAME), and password (DB_PASSWORD) to match your database configuration:
   ```bash
   DB_CONNECTION=#####
   DB_HOST=###.#.#.#
   DB_PORT=####
   DB_DATABASE=YourDatabaseName
   DB_USERNAME=YourUsername
   DB_PASSWORD=YourPassword
   ```

8. Generate an application key:
   ```bash
   php artisan key:generate
   ```

9. Run the database migrations:
   ```bash
   php artisan migrate
   ```

10. If you encounter an error "Illuminate\Database\QueryException SQLSTATE[42000]: Syntax error or access violation: 1071 Specified key was too long; max key length is 1000 bytes", You may configure the default string length by calling the Schema::defaultStringLength method within the boot method of your App\Providers\AppServiceProvider class:
    ```bash
    use Illuminate\Support\Facades\Schema;

      /**
       * Bootstrap any application services.
       */
      public function boot(): void
      {
          Schema::defaultStringLength(191);
      }
    ```
    
11. Start the development server:
    ```bash
    php artisan serve
    ```

12. The default port is 8000. If the port is already in use, you can specify a different port like this:
    ```bash
    php artisan serve --port=8080
    ```

13. Open your web browser and navigate to [http://localhost:8000](http://localhost:8000) to access your Laravel application.
<br><br><br>
## 👀 Where to find me
[![Website](https://img.shields.io/badge/Website-riajul--islam--dev.github.io-2ea44f?style=flat&logo=github)](https://riajul-islam-dev.github.io/)
[![Phone](https://img.shields.io/badge/📞_Phone-%2B8801722787007-00cc00?style=flat&amp;logo=phone)](tel:+8801722787007)
[![E-mail](https://img.shields.io/badge/Email-riajul.islam.dev@gmail.com-00cc00?style=flat&amp;logo=gmail)](mailto:riajul.islam.dev@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-riajul--islam--dev-2867B2?style=flat&logo=linkedin&logoColor=00AFF0)](https://www.linkedin.com/in/riajul-islam-dev)
[![GitHub](https://img.shields.io/badge/GitHub-riajul--islam--dev-00cc00?style=flat&logo=github)](https://github.com/Riajul-Islam-Dev)
[![Skype](https://img.shields.io/badge/Skype-riajul--islam--dev-00a2ed?style=flat&logo=skype)](https://join.skype.com/invite/y4awZfHii9yl)
[![Facebook](https://img.shields.io/badge/Facebook-ritewu2014-1877f2?style=flat&logo=facebook)](https://www.facebook.com/ritewu2014)

<p align="center">Feel free to contact 💙<p/>
