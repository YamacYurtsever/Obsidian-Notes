- The practice of using templates to generate dynamic content by combining static markup with dynamic data
- Allows developers to embed variables, expressions, and control structures directly within HTML or other markup languages

#### Template Engine
- A software component that interprets templates and generates output by replacing placeholders with actual data. 
- E.g.: Jinja (Flask), Django templates (Django)

#### Placeholders
- Syntax within the template that indicates where dynamic content should be inserted

#### Variables
```html
<p>Hello, {{ user_name }}!</p>
```

#### Conditionals
```html
{% if user_is_authenticated %}
  <p>Welcome, {{ user_name }}!</p>
{% else %}
  <p>Please log in.</p>
{% endif %}
```

#### Loops
```html
{% for fruit in fruits %}
	<li>{{ fruit }}</li>
{% endfor %}
```

#### Template Inheritance
- A feature that allows developers to create a base template with a common structure and then extend or override parts of that template in child templates

```html
<!-- base.html -->
<!DOCTYPE html>
<html>
	<head>
		<title>{% block title %}Default Title{% endblock %}</title>
	</head>
	<body>
		<div id="content">{% block content %}{% endblock %}</div>
	</body>
</html>
```

```html
<!-- page.html -->
{% extends 'base.html' %}

{% block title %}Page Title{% endblock %}

{% block content %}
	<h1>This is the content of the page.</h1>
{% endblock %}
```


