# Reusable Project CustomUser (rpcu for short)

## Description
A Reusable Django Project Template with an Auth functionality [using a custom user model](https://docs.djangoproject.com/en/2.2/topics/auth/customizing/#using-a-custom-user-model-when-starting-a-project) per the doc.


## Usage
1. clone the repo
```
git clone git@github.com:jrggementiza/Reusable_Project_CustomUser.git
```

2. Install a python3 for virtualenv
```
python3 -m venv venv
```

3. Activate virtual environtment
```
source venv/bin/activate
```

4. Install Django (and your other dependencies)
```
pip install django 2.2
```

5. Generate a requirements.txt
```
pip freeze > requirements.txt
```

6. Generate your own secret key and add export it at the bottom of your .activate file located in venv/bin/activate
```
export SECRET_KEY=‘your_secret_key'
```

7. Rename rpcu/ found in the root directory to your own "project_name" folder
``` rpcu/ => project_name/ ```

8. Rename all instances of "rpcu" found in **settings.py** to your own "project_name" found in:

The Docstring
> """ Django settings for rpcu project. ... """

ROOT_URLCONF
> **From:** ROOT_URLCONF = 'rpcu.urls' **To:** ROOT_URLCONF = 'project_name.urls'

WSGI_APPLICATION
> **From:** WSGI_APPLICATION = 'rpcu.wsgi.application' **To:** WSGI_APPLICATION = 'project_name.wsgi.application'

9. Rename "rpcu" found nn manage.py your own "project_name"

> **From:** os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'rpcu.settings' **To:** to os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'test_project.settings')

10. Migrate and Run
```
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
```

## TODO
- Style the templates better