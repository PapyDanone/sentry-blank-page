# Blank page when Sentry bundle is enabled

## Steps to reproduce:

1. clone this repo
2. `composer install`
3. add valid Sentry DSN to .env, set `APP_ENV` to `prod`
4. in `DefaultController` uncomment [this line](https://github.com/PapyDanone/sentry-blank-page/blob/master/src/Controller/DefaultController.php#L15) 
5. `php -S localhost:8000 -t public/`

<img width="732" alt="screen shot 2018-10-22 at 11 16 18 am" src="https://user-images.githubusercontent.com/804367/47301764-ae1e8000-d5ed-11e8-8654-15d62a8178c3.png">

6. Disable Sentry in bundles.php, remove `sentry.yaml`
7. in `DefaultController` comment out [this line](https://github.com/PapyDanone/sentry-blank-page/blob/master/src/Controller/DefaultController.php#L15) 
8. Clear cache
9. in `DefaultController` uncomment [this line](https://github.com/PapyDanone/sentry-blank-page/blob/master/src/Controller/DefaultController.php#L15) 

<img width="466" alt="screen shot 2018-10-22 at 11 14 06 am" src="https://user-images.githubusercontent.com/804367/47301933-313fd600-d5ee-11e8-9089-1303cc3a2216.png">
