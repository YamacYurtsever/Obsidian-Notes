- A python web framework
- Integrates with the Jinja2 [[Templating | templating]] engine

### Commands
- `flask run`

### Implementation
  
```python
from flask import Flask, render_template, request, redirect, url_for

app = Flask(__name__)

@app.route('/', methods=['GET', 'POST'])
def index():
    if request.method == 'POST':
        fruit_name = request.form.get('fruit_name')
        return redirect(url_for('thank_you', fruit_name=fruit_name))
    else:
        return render_template('index.html')

@app.route('/thank-you/<fruit_name>')
def thank_you(fruit_name):
    return f'Thank you for submitting the fruit: {fruit_name}!'
```

```html
<!DOCTYPE html>
<html lang="en">
	<head>
	    <meta charset="UTF-8">
	    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	    <title>Fruit Form</title>
	</head>
<body>
	<h1>Submit a Fruit</h1>
	<form method="post" action="{{ url_for('index') }}">
	    <label for="fruit_name">Fruit Name:</label>
	    <input type="text" id="fruit_name" name="fruit_name" required>
	    <button type="submit">Submit</button>
	</form>
</body>
</html>
```
