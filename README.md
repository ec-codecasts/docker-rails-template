# Ruby On Rails with Docker - Template

Use this code and follow the instructions below to create and run a new rails application using Docker & Docker Compose.

## Tested on

* macOS - 10.12
* Docker - 1.12.6, 1.13.0
* Docker compose - 1.9.0, 1.10.0

## Instructions / commands

```
# Go to your projects or work directory and,
git clone https://github.com/devteds/docker-rails-template.git myapp
cd myapp
rm -rf .git
docker-compose run app rails new . --force --database=mysql --skip-bundle
mv database.yml config/database.yml
docker-compose build
docker-compose up
# http://localhost:3001/
```

## Build your application

Now that you have the rails application setup, start adding features - controllers, views, models, resources, migrations etc.

## Some useful commands

```
bin/d_rails g scaffold post title body:text
# or
# docker-compose run --rm app rails g scaffold post title body:text
bin/d_rails db:migrate
bin/d_rails c
```

## Rails API-only 

If you are creating an API-only application, with no UI or web-ui components, you may change the above "rails new ..." command as,

```
docker-compose run app rails new . --force --database=mysql --skip-bundle --api
```


