This is the template that [auzigog](http://github.com/auzigog/) uses for Django project.

## Features
Pre-configured to work with:

  * [PostgreSQL](http://www.postgresql.org/)
  * [Jinja2](http://jinja.pocoo.org/docs/) templates
  * [django-debug-toolbar](http://github.com/django-debug-toolbar/django-debug-toolbar)
  * `settings_local.py.example` provided to separate machine-specific settings from universal settings


## Setup
### Typical Setup
To use normally, just clone or download the repo and use the directory structure to get you started.

### Djenesis Setup
Here's how I would typically use this template with [Djenesis](http://github.com/concentricsky/djenesis):

    # Replace all instaces of PROJECTNAME with your project name
    pip install djenesis   # Install djenesis if you haven't already

    cd ~/Projects
    djenesis PROJECTNAME/code --virtualenv=PROJECTENV/env git+https://github.com/auzigog/django-template-auzigog.git
    cd PROJECTNAME/code
    source ../env/bin/activate
    ./manage.py syncdb
    # You're ready to start coding!

Run `pip install requirements-debug.txt` to load packages that are just for local development.


## New Project Checklist
After starting a fresh project:

  1) Rename `settings_local.py.example` to `settings_local.py` and add in your database information
  1) Delete this `README.md` file, rename `README.md.example` to `README.md`, replace with information for your current project
  1) Create your first app using SAMPLEAPP as a template. These steps use
    1) Copy (don't rename) SAMPLE to a new directory for your new app. Example: `cp -R SAMPLEAPP blog`
    1) Specify new app name in `mainsite.urls`. Example: change `(r'', include('SAMPLEAPP.urls')),` to `(r'', include('blog.urls')),`
    1) Add urls, views, and templates to your new app as necessary


## License
This project is licensed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)


## Credits
Created with love by [Jeremy Blanchard](http://blanchardjeremy.com)

This project originated from [csky-django-template](https://github.com/concentricsky/csky-django-template)