# medium-laravel-angular-auth
Laravel &amp; Angular authentication Medium article resources

# Steps to make it works
1. Clone this repository
2. Install laravel project dependencies
```
cd medium-laravel-angular-back
composer install
```
3. Install angular project dependencies
```
cd medium-laravel-angular-front
npm install
```
4. Create an `.env` file and configure your database access
5. Migrate and configure laravel/passport
```
cd medium-laravel-angular-back
php artisan migrate
php artisan passport:install
```
6. Configure laravel/passport on Angular
```
Get the password grant client token generated by the above command (php artisan passport:install) and update the file
laravel-angular-auth-front/src/app/services/auth.service.ts
by editing the login() method
```
7. Add sample user
```
cd medium-laravel-angular-back
php artisan db:seed
```
This command will add a sample user with the following information to your database:
- Name: **John DOE**
- Email: **john.doe@email.com**
- Password: **secret**
8. Run application
Run laravel application, by executing the following command:
```
cd medium-laravel-angular-back
php artisan serve
```
Run angular application, by executing the following command:
```
cd medium-laravel-angular-front
ng serve
```

PS. Use the sample user email and password in the authentication form.
