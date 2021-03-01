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
