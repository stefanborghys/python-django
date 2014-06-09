python-django
=============

A Python Django framework tryout.

After downloading Python i decided to tryout the Django framework.</br>
I got a version from the GitHub project:
<a href="https://github.com/django/django/tree/stable/1.7.x">https://github.com/django/django/tree/stable/1.7.x</a>

Installing Django on Mac OS X
-----------------------------
<ol>
	<li>open IDLE (installed with Python)</li>
	<li>can django be found?</br>
		Command:</br>
		<code>import django</code></br>
		<code>print(django.get_version())</code>
	</li>
	<li>if not, is django on Python's search path?
		<ol>
			<li>print Python's search path</br>
				Command:</br>
				<code>import sys</code></br>
				<code>print(sys.path)</code></br>
				</br>
				Output:</br>
				<code>
	['', '/Users/user-name/Documents', '/Library/Frameworks/Python.framework/Versions/3.4/lib/python34.zip', '/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4', '/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4/plat-darwin', '/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4/lib-dynload', '/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4/site-packages']
				</code></br>
				</br>
				We now know that the site-packages directory can be found in:</br>
				/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4/site-packages</br>
				</br>
				source: <a href="https://docs.python.org/2/install/index.html#modifying-python-s-search-path">https://docs.python.org/2/install/index.html#modifying-python-s-search-path</a>
			</li>
			<li>request Python's site-packages directory</br>
				Another way to find the site-packages directory is by executing following,</br>command:</br>
				<code>python -c "from distutils.sysconfig import get_python_lib; print(get_python_lib())"</code></br>
				</br>
				source: <a href="https://docs.djangoproject.com/en/1.6/topics/install/#id1">https://docs.djangoproject.com/en/1.6/topics/install/#id1</a>
			</li>
		</ol>
	</li>
	<li>add django's path to Python's search</br>
		Add a new django.pth file in folder:</br>
		/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4/site-packages/ </br>
		containing the path to the django framework:</br>
		/Users/<user-name>/Documents/projects/github/python-django/django/django-stable-1.7.x</br>
		</br>
		source: <a href="https://docs.djangoproject.com/en/1.6/topics/install/#id1">https://docs.djangoproject.com/en/1.6/topics/install/#id1</a>
	</li>
	<li>restart IDLE</li>
	<li>retry step 2</br>
		Command:</br>
		<code>import django</code></br>
		<code>print(django.get_version())</code></br>
		</br>
		Output:</br>
		<code>1.7b4</code>
	</li>
</ol>