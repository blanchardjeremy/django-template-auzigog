This is the template that I use for my Django projects.

## Features

  * [PostgreSQL](http://www.postgresql.org/) and [psycopg2](http://pypi.python.org/pypi/psycopg2)
  * [django-debug-toolbar](http://github.com/django-debug-toolbar/django-debug-toolbar) and `requirements-debug.txt`
  * [Jinja2](http://jinja.pocoo.org/docs/) and [jingo](http://github.com/concentricsky/jingo) support
  * `settings_local.py.example` provided to separate machine-specific settings from universal settings


## Usage
### Typical
To usually normally, just clone or download the repo and use the directory structure to get you started.

### Example with Djenesis
Here's how I would typically use this template with [Djenesis](http://github.com/concentricsky/djenesis):

    # Replace all instaces of PROJECTNAME with your project name

    # Install djenesis if you haven't already
    pip install djenesis

    cd ~/Projects
    djenesis PROJECTNAME/code --virtualenv=PROJECTENV/env git+https://github.com/auzigog/django-template-auzigog.git
    cd PROJECTNAME/code
    source ../env/bin/activate
    ./manage.py syncdb
    # You're ready to start coding!

    # Optionally start a git repo inside the `code` directory
    git init
    git add -A
    git commit -m 'Big bang! Initial commit of PROJECTNAME'

The `requirements-debug.txt` file can be used to specify packages you use on your local development environment.

    pip install requirements-debug.txt

After installation:

  * Search all instances of SAMPLEAPP and replace them with your first app name
  * Rename `settings_local.py.example` to `settings_local.py` and add in your database information

The run:

    cd ~/Projects/PROJECTNAME/code
    ./manage.py syncdb

## License
This project is licensed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)


## Credits
Created by [Jeremy Blanchard](http://blanchardjeremy.com)