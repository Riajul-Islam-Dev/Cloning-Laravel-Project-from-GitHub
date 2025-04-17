# Laravel Project Setup Guide

Follow these steps to clone and set up a Laravel project from GitHub:

1. **Clone the repository:**

   ```bash
   git clone <GitHub Repository URL>
   ```

2. **Navigate to the cloned repository:**

   ```bash
   cd <Cloned project name>
   ```

3. **Install dependencies:**

   ```bash
   composer install
   ```

   If you encounter errors due to outdated packages, update the dependencies:

   ```bash
   composer update
   ```

4. **Copy the environment file:**

   ```bash
   cp .env.example .env
   ```

   If the `cp` command is unavailable (e.g., on Windows), use:

   ```bash
   copy .env.example .env
   ```

5. **Edit database configuration in .env:**

   ```
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=YourDatabaseName
   DB_USERNAME=YourUsername
   DB_PASSWORD=YourPassword
   ```

6. **Generate application key:**

   ```bash
   php artisan key:generate
   ```

7. **Run database migrations:**

   ```bash
   php artisan migrate
   ```

8. **Start the server:**

   ```bash
   php artisan serve
   ```

   By default, the server runs on port `8000`. If the port is already in use, specify another:

   ```bash
   php artisan serve --port=8080
   ```

9. **Access the application at:**
   [http://localhost:8000](http://localhost:8000)

### Common Error:

If you encounter the error:

```
Illuminate\Database\QueryException SQLSTATE[42000]: Syntax error or access violation: 1071 Specified key was too long; max key length is 1000 bytes
```

Add the following code to the `boot` method in `App\Providers\AppServiceProvider`:

```php
use Illuminate\Support\Facades\Schema;

/**
 * Bootstrap any application services.
 */
public function boot(): void
{
    Schema::defaultStringLength(191);
}
```

---

## Contact Me

If you have any questions or need assistance, feel free to reach out:

[![Website](https://img.shields.io/badge/Website-riajul.islam.softkit.io-2ea44f?style=flat&logo=github)](https://riajul.islam.softkit.io/)
[![Phone](https://img.shields.io/badge/%F0%9F%93%9E_Phone-%2B8801722787007-00cc00?style=flat&logo=phone)](tel:+8801722787007)
[![E-mail](https://img.shields.io/badge/Email-riajul.islam.dev@gmail.com-00cc00?style=flat&logo=gmail)](mailto:riajul.islam.dev@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-riajul--islam--dev-2867B2?style=flat&logo=linkedin)](https://www.linkedin.com/in/riajul-islam-dev)
[![GitHub](https://img.shields.io/badge/GitHub-riajul--islam--dev-00cc00?style=flat&logo=github)](https://github.com/Riajul-Islam-Dev)
[![Skype](https://img.shields.io/badge/Skype-riajul--islam--dev-00a2ed?style=flat&logo=skype)](https://join.skype.com/invite/y4awZfHii9yl)
[![Facebook](https://img.shields.io/badge/Facebook-RiajulIslamDEV-1877f2?style=flat&logo=facebook)](https://www.facebook.com/RiajulIslamDEV)

<p align="center">Feel free to connect! 💙</p>
