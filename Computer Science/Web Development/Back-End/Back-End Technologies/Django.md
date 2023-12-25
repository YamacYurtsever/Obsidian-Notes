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
```
myproject/
|-- manage.py
|-- myproject/
|   |-- __init__.py
|   |-- settings.py
|   |-- urls.py
|   |-- asgi.py
|   |-- wsgi.py
|-- myapp/
|   |-- migrations/
|   |-- __init__.py
|   |-- admin.py
|   |-- apps.py
|   |-- models.py
|   |-- tests.py
|   |-- views.py
|-- static/
|-- templates/
```