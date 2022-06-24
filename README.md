# Django_Unchained
Python startup project with django framework

This file is to write all the necessary information about when and how the project is changed.

To create django project, check if you have installed django with command:
    py -m django --version

If django exists in the system, create project with:
    py -m django startproject project001

The further steps are followed from the website: https://docs.djangoproject.com/en/4.0/intro/tutorial01/.
    "project001" is named by me. The website named it as "mysite".

For Migrations:
    1. Add models to models.py.
    2. Include models.py app's config in main app's settings.py (in INSTALLED_APPS array).
        * In this app, we include 'polls.apps.PollsConfig'.
    3. Now run
        a. py manage.py makemigrations 'migration_name' -> create new migration.
        b. py manage.py sqlmigrate 'migration_name' 'number before initial.py' -> gives sql commands that run after migration.
        c. py manage.py migrate -> runs migration to the sql db.

-------DATABASE API-------
    Basically django's ORM

    You can directly use objects created from models.py and save them to the database.
    These objects serve you sql statements. For instance, object.save() - saves created object (row) to db.