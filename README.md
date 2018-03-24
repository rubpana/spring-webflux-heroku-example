# spring-webflux-heroku-example
Demo project for Spring webflux deployed on Heroku

## Initial setup on Heroku
- Create an application on Heroku
- From the root folder of this git project, run:
```sh
$ heroku login
# Commit all your changes
$ git add .
$ git commit -m "Initial commit"
# Adding Heroku's remote git repository to this git repository (locally)
$ heroku git:remote -a spring-web-dev
$ git pull heroku
$ git push heroku master
```

The application will be compiled and run. Although the tomcat server will be running at port XXXX, Heroku exposes your MVC application from:
https://spring-web-dev.herokuapp.com/. So, to test the API, you must invoke: https://spring-web-dev.herokuapp.com/test

## Running Locally

```sh
$ heroku local
```

It will serve at port 8080

## Deploying to Heroku

So Heroku deploys your application, you must push your changes to the master branch, if not your changes won't be compiled and deployed by Heroku.

```sh
$ heroku login
# Commit all your changes
$ git push heroku master
```