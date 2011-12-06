These are project templates that I use for my Django projects.

## Features
The **normal** template includes:
  * [PostgreSQL](http://www.postgresql.org/) and [psycopg2](http://pypi.python.org/pypi/psycopg2)
  * [django-debug-toolbar](http://github.com/django-debug-toolbar/django-debug-toolbar) and `requirements-development.txt`
  * [Jinja2](http://jinja.pocoo.org/docs/) and [jingo](http://github.com/concentricsky/jingo) support
  * `settings_local.py.example` provided to separate machine-specific settings from universal settings


## Usage
First, get a copy of this repo by cloning it or downloading it. Place the repo in a folder of your choice (for example, `~/Projects/django-project-templates/`)

Here's how I would typically use this template with [djenesis](http://github.com/concentricsky/djenesis):

    cd ~/Projects
    mkdir newproject # Replace all isntaces of newproject with your project name
    cd newproject
    djenesis code --virtualenv=env --template=~/Projects/django-project-templates/normal
    cd code
    source ../env/bin/activate
    # Ready to start coding!

    # Optionally start a git repo inside the `code` directory
    git init
    git add *
    git commit -m 'Big bang! Initial commit of newproject'

To make full use of the `normal` template, make sure to install the other requirements file:

    pip install requirements-development.txt

## License
This project is licensed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)


## Credits
Released