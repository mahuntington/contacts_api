# Deployment Instructions

## Local Installation

### Create Local Repo

- Fork this repo and then clone the fork to your local computer
- Make sure you are using a `venv` python environment
	- e.g. `source ~/ga-env/bin/active`
	- create a new environment and use that
- Install dependencies with `python -m pip install -r requirements.txt`

### Postgres

- Open app Postgres App
- From menu icon, next to "New Server", choose "Start" and then "Open Postgres"
- Double click on a sub-database and, in the terminal window that opens, run `CREATE DATABASE django_contacts` to create the sub database

### In Terminal

- Run `python manage.py migrate` to set up the tables in the DB
- Run `python manage.py runserver` to start the server

## Deploy to Heroku

- Run `heroku create` to create heroku app
- Copy url of heroku app created (e.g. `blooming-fjord-06511.herokuapp.com`) and add it to `ALLOWED_HOSTS` in `django_rest_api/settings.py`
	e.g. `ALLOWED_HOSTS = ['localhost', 'desolate-thicket-29906.herokuapp.com']`
- add/commit to git.  Then run `git push heroku master` 
- run `heroku run bash` to enter bash and then run `python manage.py migrate` and `python manage.py createsuperuser` (follow prompts) and then `exit` 
- run `heroku open` to open remote app
