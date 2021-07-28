# test-web on heroku

## Requirements

* Heroku CLI [install instructions](https://devcenter.heroku.com/categories/command-line)
* Docker


## Instructions

1. 
    export APP_NAME=heroku-app-name
    export HEROKU_API_KEY=api-key

2. 
    heroku container:login

3. 
    heroku container:push -a $APP_NAME web
    heroku container:release -a $APP_NAME web

4.
    https://schemaspytest.herokuapp.com