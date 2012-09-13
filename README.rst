=====================
Django-Sphinx-autodoc
=====================


Django is awesome in that way you can reuse a lot of applications in your
projects. It means for big projects that you'll get a long list of applications
in your settings.INSTALLED_APP.

If you're using Django with Sphinx and want to autodoc all these apps in a wink
of an eye, then this app is for you.


How it works
------------

It will scrape all your .py files in each application listed by INSTALLED_APP,
then add automodules in your PROJECT/SPHINX_ROOT/modules.rst.


Install
-------

I suggest importing this code into your project as a git submodule.


Usage
-----

``$ django-sphinx-autodoc/generate_autodoc.py``


Settings
--------

You can modify some of the settings used by django-sphinx-autodoc:

- **DS_ROOT**: root path for documentation, relative to the generate_autodoc.py script (defaults to "../docs")
- **DS_MASTER_DOC**: name of your master document (defaults to "index.rst")
- **DS_FILENAME**: name for the modules (defaults to "auto_modules.rst")
- **DS_DOC_TITLE**: title for the modules page (defaults to ``DS_FILENAME``)
- **DS_EXCLUDED_APPS**: list of applications to exclude (defaults to [])
- **DS_EXCLUDED_MODULES**: list of files to exclude (default to ["\_\_init\_\_.py"])


TODO
----

v1
++

- Include external apps (currently only internal apps, located in the project
  root directory)
- Write tests
- improve the not_relevant stuff to auto exclude a file without class or def

v2
++

Django command extension to update the autodoc
