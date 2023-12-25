- A python web framework

### Features
- Has an [[ORM]] called Django Models
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
! Changes to the models script need to be migrated to be applied