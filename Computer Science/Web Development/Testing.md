- A crucial process aimed at identifying and fixing errors or defects in software to ensure its reliability, functionality, and performance.

### Unit Testing
- Individual units or components of a system are tested in isolation to ensure they function as intended, in isolation from the rest of the application
- `assert` returns error if the condition fails:
```python
def square(x):
	return x * x;

assert square(10) == 100;
```
- Unit testing methods:
	- `assertEqual`
	- `assertNotEqual`
	- `assertTrue`
	- `assertFalse`
	- `assertIn`
	- `assertNotIn`
	  
### Simulating HTTP Requests
- Creating and sending mock or simulated [[HTTP Requests]] to a web server or [[APIs | API]] in a controlled environment
- This allows developers to test the behavior of their web applications or [[APIs]] without relying on real user interactions or external services

Django
```python
def test_index(self):
	c = Client()
	response = c.get("/flights/")
	self.assertEqual(response.status_code, 200)
```
! When testing Django creates a separate testing [[Types of Databases | database]] so that the actual database is not affected by the operations in the tests

### Automated Browser Testing
- Using automated scripts and tools to simulate user interactions with a web application across different web browsers
- E.g.: Selenium

