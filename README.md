#SITCOM

This project is an app building exercise focusing on Python/Django, PostgresQL and Ted Mosby.

##Virtualenv Setup
If you do not have virtualenv installed: `https://virtualenv.pypa.io/en/stable/installation/`

##Postgres Setup

###Creating a new user and database:
- Change to user postgres:
`sudo su - postgres`
- Enter psql cli:
`psql`

- Create db:
`CREATE DATABASE sitcom;`

`CREATE USER sitcom with password 'sitcom_db';`
`ALTER ROLE myprojectuser SET client_encoding TO 'utf8';`
`ALTER ROLE myprojectuser SET default_transaction_isolation TO 'read committed';`
`ALTER ROLE myprojectuser SET timezone TO 'UTC';`
`GRANT ALL PRIVILEGES ON DATABASE sitcom_db TO sitcom;`

Use \q to exit psql cli then,
Use 'exit' to return to default user permissions in cli


DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': 'sitcom_db',
        'USER': 'sitcom',
        'PASSWORD': 'sitcom_db',
        'HOST': 'localhost',
        'PORT': '',
    }
}

