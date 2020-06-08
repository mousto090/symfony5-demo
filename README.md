# Symfony 5 demo
A tiny Symfony 5 App Demo

## Development

`composer install` install dependencies

`npm install` install node dependencies

`symfony server:start -d` start symfony server

`npm run watch` build and watch assets

## Deploying to Heroku
Steps to deploy the app to Heroku

`heroku create symfony5-heroku --region eu`

`heroku config:set APP_ENV=prod`

By default the app use only one buildpack, the `heroku/php` buildpack,
as we use `webpack-encore` to manage or assets, we must add the
`nodejs` buildpack to build our assets.

`heroku buildpacks:set heroku/php`

`heroku buildpacks:add --index 1 heroku/nodejs`

Finaly

`git push heroku master`