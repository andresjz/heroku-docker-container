# test-web on heroku

The main goal of this repository is to allow you to deploy static content adding a basic security layer, since heroku support the deployment of container, you can easily create your custom configuration, in this case using basic authentication, however you can implement other configurationif you want
## Requirements

* Heroku CLI [install instructions](https://devcenter.heroku.com/categories/command-line)
* Docker

## Instructions
0. 

Login to heroku `heroku login`
If you don't have an app created yet, you can run `heroku create`


1. 
```
    export APP_NAME=heroku-app-name
    export HEROKU_API_KEY=api-key
```

2. 
```
    heroku container:login
```

3. 
```
    heroku container:push -a $APP_NAME web
    heroku container:release -a $APP_NAME web
```

4. 
    run `heroku open -a $APP_NAME web`
    https://$APP_NAME.herokuapp.com

5. to see the logs `heroku logs --tail -a $APP_NAME`