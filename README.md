# Blank page when Sentry bundle is enabled

## Steps to reproduce:

1. clone this repo
2. `composer install`
3. add valid Sentry DSN to .env
4. in `DefaultController` uncomment [this line](https://github.com/PapyDanone/sentry-blank-page/blob/master/src/Controller/DefaultController.php#L15) 
5. `php -S localhost:8000 -t public/`

