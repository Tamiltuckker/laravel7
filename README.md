## About Laravel Authentication

Authentication and authorisation are critical security elements on all websites and applications. To make sure our developers are up to speed we put this information together as a primer on authentication within Laravel. The members of our team not already familiar with some of the terminology have found it useful so we’ve decided to share it with you.

**Authentication:**
- Confirming your identity (typically with user/password combination for example).
### Authentication Steps for larvel 7:

**Install require laravel 7:**
- composer create-project --prefer-dist laravel/laravel laravel_study "7.*"

 **Require laravel/ui for larvel 7:**
- composer require laravel/ui "^2.1" --dev

**Generate Auth:**
- php artisan ui bootstrap --auth

**Install NPM:**
- npm install

**Run NPM:**
- npm run dev
## Refer Article Links:
- [Laravel-7 authentication simple way](https://www.itsolutionstuff.com/post/laravel-6-auth-login-with-username-or-email-tutorialexample.html).

- [Auth Routes](https://stackoverflow.com/questions/39196968/laravel-5-3-new-authroutes).

## Adding new Routes:
- Auth::routes();
## about Auth routes:
- Auth::routes() is just a helper class that helps you generate all the routes required for user authentication.
Here are the routes

## Authentication Routes...

- $this->get('login', 'Auth\LoginController@showLoginForm')->name('login');
- $this->post('login', 'Auth\LoginController@login');
- $this->post('logout', 'Auth\LoginController@logout')->name('logout');

## Registration Routes...

- $this->get('register', 'Auth\RegisterController@showRegistrationForm')->name('register');
- $this->post('register', 'Auth\RegisterController@register');

## Password Reset Routes...

- $this->get('password/reset', 'Auth\ForgotPasswordController@showLinkRequestForm');
- $this->post('password/email', 'Auth\ForgotPasswordController@sendResetLinkEmail');
- $this->get('password/reset/{token}', 'Auth\ResetPasswordController@showResetForm');
- $this->post('password/reset', 'Auth\ResetPasswordController@reset');
## Check Route List (After added Auth routes in Web.php):

- php artisan route:list

## Added username (or) Email Authentication:
## Followed this steps:

- Laravel has created default login blade file. we need to add comman username field on it and remove email field.

**Migrations and model**

- php artisan make:migration add_username_to_users_table --table=users
- php artisan migrtae
- In User  model file add  to username field.

**Controller**

- Login[Add findUsername() and username() function then add to this function in consrtuct method]
- Register [Add username field]

**Blade**
- [resources/views/auth/login.blade.php](https://www.codecheef.org/article/laravel-auth-login-with-email-or-username-in-one-field).

- Add Username field in Register blade 


**



