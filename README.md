# README

Rails6, MySQL5.7 on mac Docker 

```
$ docker-compose run web rails new . --skip-action-mailer --skip-active-storage --skip-action-cable -d mysql
```

database.yml
```
default: &default
  adapter: mysql2
  encoding: utf8mb4
  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>
  username: root
  password:
  host: db  
```

```
$ docker-compose run web rake db:create
$ docker-compose up web  
$ docker-compose down
```
