## Django
### What is Django?


### Django components


### Using Django


#### set virtual env
Virtual env keeps all required libraries loaded and a set of pre-requisites for you app. 

This keeps dependencies isolated from other apps. 

There are a few virtual env managers, the most common are:
* conda
* pip
* pyenv


In order to create virtual env,  you need  to execute this command on a terminal.
```shell
py -m venv env
```

activate virtual env (Windows)
```shell
./env/Scripts/activate.bat
```

activate virtual env (Mac)
```shell
source env/bin/activatee
```

deactivate virtual env
```commandline
deactivate
```

### Setting up a Django app
installing Django
```shell
pip install Django~=3.2.10
```
Create Django Main App (Mac)
```shell
django-admin startproject mysite .
```

Create Django Main App (Windows)
```shell
django-admin.exe startproject mysite .
```

to configure Django you need to edit `project/settings.py` file
```shell
TIME_ZONE = 'Europe/Berlin'
...
LANGUAGE_CODE = 'es-es'
...
STATIC_URL = '/static/'
STATIC_ROOT = BASE_DIR / 'static'
ALLOWED_HOSTS = ['127.0.0.1', '.pythonanywhere.com']
...
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': os.path.join(BASE_DIR, 'db.sqlite3'),
    }
}
```

After update settings you need to migrate recent changes

```shell
python manage.py migrate
```

#### Running Django app

Execute next commands in Terminal/console from project's folder
```shell
python manage.py runserver
```

If everything goes as expected you will get an output like this
```shell
Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).
August 17, 2022 - 22:59:15
Django version 3.2.15, using settings 'project.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CTRL-BREAK.


```


### create your app
```shell
python manage.py startapp blog
```

Where:

`manage.py` stands for Django framework manager

`startapp` makes reference to a Django app template

`blog` is your app name

## Useful links

* https://tutorial.djangogirls.org/es/

## Next steps:

### Security
* https://opensource.com/article/18/1/10-tips-making-django-admin-more-secure

### ORM
* https://steelkiwi.com/blog/best-practices-working-django-models-python/

### Unit tests
* https://www.digitalocean.com/community/tutorials/how-to-add-unit-testing-to-your-django-project-es