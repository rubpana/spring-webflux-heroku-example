# spring-webflux-heroku-example
Demo project for Spring webflux deployed on Heroku

## Initial setup on Heroku (It works for any Java project)
- Create an application on Heroku named "spring-web-dev"
- From the root folder of this git project, run:
```sh
$ heroku login
# Download the repository and commit all your changes
$ git clone https://github.com/rubpana/spring-webflux-heroku-example.git
$ cd spring-webflux-heroku-example
$ git add .
$ git commit -m "Initial commit"
# Adding Heroku's remote git repository to this git repository (locally)
$ heroku git:remote -a spring-web-dev
# Uploading your changes to Heroku repo
$ git push heroku master
# Uploading your changes to your repo
$ git push
```

To check out the Heroku logs during the deployment:
```sh
$ heroku logs -t
```

The application will be compiled and run. Although the tomcat server will be running at port XXXX, Heroku exposes your MVC application at:
```
https://spring-web-dev.herokuapp.com/
```
So, you must invoke: ```https://spring-web-dev.herokuapp.com/test``` to test the API exposed for this project.

## Running Locally

```sh
$ heroku local
```

It will serve your application at port 5000.

## Making changes on the project and deploying them to Heroku

So Heroku deploys your application, you must push your changes to the master branch, not to your develop branch, if not your changes won't be compiled and deployed by Heroku. The steps are quite similar to the initial setup steps.

```sh
$ heroku login
$ git clone https://github.com/rubpana/spring-webflux-heroku-example.git
$ cd spring-webflux-heroku-example
$ git add .
$ git commit -m "CHANGES"
# Uploading your changes to Heroku repo
$ git push heroku master
# Uploading your changes to your repo
$ git push
```