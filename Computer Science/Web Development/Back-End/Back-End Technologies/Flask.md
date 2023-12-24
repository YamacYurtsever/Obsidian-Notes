- A python web framework
- Integrates with the Jinja2 templating engine
  
```python
from flask import Flask, render_template, request app = Flask(__name__) @app.route('/', methods=['GET', 'POST']) def index(): if request.method == 'POST': # Handle POST request fruit_name = request.form.get('fruit_name') return f'You submitted the fruit: {fruit_name} via POST request.' else: # Handle GET request return render_template('index.html')
```