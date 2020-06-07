# Codebase Django

- Codebase Django is a guide to boost ready-to-use Django code.
- Powered by [Cookiecutter ](https://github.com/cookiecutter/cookiecutter "Cookiecutter ").
- Thanks to [Pablo Trinidad](https://github.com/pablotrinidad "Pablo Trinidad")

#### Features
- With Django 2.2.13
- Works with Python 3.8
- Work with PostgreSQL 10.5, but customizable.
- Optimized development and production settings.
- Send emails via [Anymail](https://github.com/anymail/django-anymail "Anymail") (using [Mailgun](https://www.mailgun.com/ "Mailgun") by default).
- Docker support using docker-compose for development.
- Default integration with pre-commit for identifying simple issues before submission to code review.


#### Constraints
- Only maintained 3rd party libraries are used.
- Uses PostgreSQL everywhere.
- Environment variables for configuration (This won't work with Apache/mod_wsgi).


#### Usage
Suppose you want to create a Django project. Instead, use this and then edit and generate results. If there are configuration problems send your corrections.

#### Contributing
I will be happily accepting pull requests from anyone.

#### Development
- Now run it against this repo:
`$ https://github.com/LhernerRemon/Codebase_basic_Django`
- And run on your console::
`$ git clone https://github.com/LhernerRemon/Codebase_basic_Django.git`

- Then, to be able to run and start the codebase with Docker:
```
docker-compose build
docker-compose up
```
Warning: This code is in development, we know that nothing is perfect, but it can already be used. I'm improving it.

#### Collaborators
[Lherner Remón](https://github.com/LhernerRemon "Lherner Remón") | UNSCH Systems Engineering Student | lherner.remon.27@unsch.edu.pe
