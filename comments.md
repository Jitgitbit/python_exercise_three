pip3 install django
django-admin

REMOVING from git locally
1) (first remove it from github)
2) rm -rf <python-exercise-two>/.git   NOPE -->  in directory:   rm -rf .git
3) (now remove the directory itself too)

START:
django-admin startproject python_exercise_two

git init
git add .
git commit -m 'first'
gst
and then the github stuff...
git remote add origin git@github.com:Jitgitbit/python_exercise_two.git
git push -u origin master
gst
DONE

python3 manage.py runserver    ------>   http://127.0.0.1:8000/   

(wsgi.py is for deployment)

python3 manage.py startapp blog ---> create a blog app within the project !
python3 manage.py startapp portfolio ---> create a portfolio app within the project !

python3 -m pip install Pillow

python3 manage.py migrate
python3 manage.py makemigrations
python3 manage.py migrate

python3 manage.py createsuperuser
thierrydekelver
django1234 (python3 manage.py changepassword username)

python3 manage.py makemigrations
python3 manage.py migrate

------------------------
INSIDE Python Anywhere:
dashboard, bash
(linux-server)
ls
pwd
git clone https://github.com/Jitgitbit/python_exercise_three.git
ls
------------------------
INSIDE Python Anywhere:
dashboard, bash
(linux-server)
ls
mkvirtualenv --python=/usr/bin/python3.8 portfoliovenv
python
exit()
deactivate
cd .virtualenvs
ls
cd ..
workon portfoliovenv
pip install django pillow
-----------------------
INSIDE Python Anywhere:
dashboard, bash
(linux-server)
ls
cd python_exercise_three/
pwd
ls

OPEN UP NEW TAB
INSIDE Python Anywhere:
web, +add a new web app, next, Manual configuration, next, Enter path to a virtualenv, if desired :
portfoliovenv
Enter the path to your web app source code :
/home/thierryD/python_exercise_three
Go to directory
python_exercise_three/
settings.py
DEBUG = False
ALLOWED_HOSTS = ['thierryD.pythonanywhere.com']
HIT SAVE
CLICK ON PYTHONLOGO (left corner) to go back, web, HIT Reload thierryD.pythonanywhere.com
Working directory:
/home/thierryD/python_exercise_three

INSIDE WSGI configuration file:

ONLY LEAVE:
# +++++++++++ DJANGO +++++++++++
# To use your own django app use code like this:
#import os
#import sys
#
## assuming your django settings file is at '/home/thierryD/mysite/mysite/settings.py'
## and your manage.py is is at '/home/thierryD/mysite/manage.py'
#path = '/home/thierryD/mysite'
#if path not in sys.path:
#    sys.path.append(path)
#
#os.environ['DJANGO_SETTINGS_MODULE'] = 'mysite.settings'
#
## then:
#from django.core.wsgi import get_wsgi_application
#application = get_wsgi_application()

AND THEN:
import os
import sys

# assuming your django settings file is at '/home/thierryD/mysite/mysite/settings.py'
# and your manage.py is is at '/home/thierryD/mysite/manage.py'
path = '/home/thierryD/mysite'
if path not in sys.path:
    sys.path.append(path)

os.environ['DJANGO_SETTINGS_MODULE'] = 'mysite.settings'

# then:
from django.core.wsgi import get_wsgi_application
application = get_wsgi_application()

AND THEN:
import os
import sys

# assuming your django settings file is at '/home/thierryD/mysite/mysite/settings.py'
# and your manage.py is is at '/home/thierryD/mysite/manage.py'
path = '/home/thierryD/python_exercise_three'
if path not in sys.path:
    sys.path.append(path)

os.environ['DJANGO_SETTINGS_MODULE'] = 'python_exercise_three.settings'

# then:
from django.core.wsgi import get_wsgi_application
application = get_wsgi_application()

HIT SAVE
CLICK ON PYTHONLOGO (left corner) to go back, web, HIT Reload thierryD.pythonanywhere.com

OPEN UP NEW TAB
thierryD.pythonanywhere.com