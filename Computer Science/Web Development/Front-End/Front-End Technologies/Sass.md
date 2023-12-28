- Sass (Syntactically Awesome Stylesheets) is a preprocessor scripting language that is interpreted or compiled into [[HTML, CSS & JavaScript#CSS (Cascading Style Sheets) | CSS]]
- It adds a layer of abstraction and functionality to CSS, making stylesheets more maintainable and efficient

#### Features
- **Variables**
```scss
$primary-color: #3498db;

body {
    background-color: $primary-color;
}
```
- **Nesting**
```scss
nav {
    ul {
        margin: 0;
        padding: 0;
        list-style: none;

        li {
            display: inline-block;
            margin-right: 10px;

            a {
                text-decoration: none;
            }
        }
    }
}
```
- **Mixins**
```scss
@mixin border-radius($radius) {
    -webkit-border-radius: $radius;
    -moz-border-radius: $radius;
    border-radius: $radius;
}

.box {
    @include border-radius(10px);
}
```
- **Inheritance**
```scss
.error {
    border: 1px solid #ff0000;
    color: #ff0000;
}

.important-error {
    @extend .error;
    font-weight: bold;
}
```