python-django
=============

A Python Django framework tryout.

After downloading Python i decided to tryout the Django framework.
I got a version from the GitHub project:
https://github.com/django/django/tree/stable/1.7.x

Installing Django
-----------------

1. open IDLE (installed with Python)
2. can django be found?
Command:
import django
print(django.get_version())

3. no, is django on Python's search path?
3.1 print Python's search path
Command:
import sys
print(sys.path)

Output:
['', '/Users/<user-name>/Documents', '/Library/Frameworks/Python.framework/Versions/3.4/lib/python34.zip', '/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4', '/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4/plat-darwin', '/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4/lib-dynload', '/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4/site-packages']

We now know that the site-packages directory can be found in:
/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4/site-packages

source: https://docs.python.org/2/install/index.html#modifying-python-s-search-path

Another way to find the site-packages directory is by executing following command:
python -c "from distutils.sysconfig import get_python_lib; print(get_python_lib())"

source: https://docs.djangoproject.com/en/1.6/topics/install/#id1

3.2 add django's path to Python's search
Add a new django.pth file in folder: 
/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4/site-packages/ 
containing the path to the django framework:
/Users/<user-name>/Documents/projects/github/python-django/django/django-stable-1.7.x

source: https://docs.djangoproject.com/en/1.6/topics/install/#id1

3.3 restart IDLE
4 retry step 2
Output:
1.7b4

source: https://docs.python.org/2/install/index.html#modifying-python-s-search-path
