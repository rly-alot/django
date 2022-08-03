# Getting Started

## Table of Contents

- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
  - [Running the Webserver](#running-the-webserver)
  - [Application Routes](#application-routes)
  - [Creating an Admin user](#creating-an-admin-user)
  - [Managing the DB](#managing-the-db)
- [Project Structure](#project-structure)
- [Documentation](#documentation)
- [Useful Commands](#useful-commands)

---

## Requirements

- Python     >= 3.8.5
- Django     >= 3.1.1

---

## Installation

Create a virtual environment called 'env' using Python3.8
Then activate your enviornment

```bash
virtualenv -p Python3.8 env
source env/bin/activate
```

Install all requirements using pip
NOTE: please ensure you are in the repo's root directory

```bash
pip install -r requirements.txt
```

---

## Usage

### Running the Webserver

To run the webserver during development; ensure you are in your virtual environment

```bash
python ./devalot/manage.py runserver
```

This will run a small webserver at 127.0.0.1:8000

### Application Routes

Append to 127.0.0.1:8000

- /admin/
  - This is to access the Django admin login page
  - Dev use only!!
- /app/index/
  - Webapp's index and main entry point

### Creating an Admin User

1. Use manage.py to create an admin user

```bash
python manage.py createsuperuser
```

2. Enter desired username
3. Enter desired email (optional)
4. Enter desired password

### Managing the DB

To synchronize changes made in the models

```bash
# Updating Django models (and subsequent DB schema)
python manage.py makemigrations app

# Updating DB to match Django models
python manage.py migrate

# Checking (for errors) migrations before making migrations
python manage.py check
```

To remove all data from the DB

```bash
# Removes all data from DB
# BUT DOES NOT RESET AUTO_INCREMENT COUNTER
# (will continue from last pk)
python manage.py flush
```

---

## Project Structure

```

```

---

## Documentation

https://devalot.readthedocs.io/en/latest/index.html

---

## Useful commands

Print project directory

```bash
tree -I 'env|__pycache__' .
```

Django Import Export DB

```
https://dev.to/coderasha/how-to-export-import-data-django-package-series-3-39mk
```
