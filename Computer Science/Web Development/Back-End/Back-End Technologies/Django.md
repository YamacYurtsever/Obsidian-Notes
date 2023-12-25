- A python web framework

### Features

- Has an [[ORM]] called Django Models
	! Changes to the models script need to be migrated to be applied
	- Creating
		- `class MyModel(models.Model):`
		- `MyModel.objects.create()`
	- Reading
		- `MyModel.objects.get()`
		- `MyModel.objects.all()`
	- Updating
		- `example_object.save()`
	- Deleting
		- `example_object.delete()`
- Has its own [[Templating | templating]] engine
- Has a built-in admin interface
- Handles authentication, authorization and security features such as CSRF tokens

### Project Structure
![[Django 2023-12-25 18.59.02.excalidraw | 500]]

### Commands
- `django-admin startproject <projectname>`
- `python manage.py startapp <appname>`
- `python manage.py runserver`
- `python manage.py createsuperuser`
- `python manage.py test`
- `python manage.py makemigrations`
- `python manage.py migrate`
- `python manage.py shell` -> Can run database commands



