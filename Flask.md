
![header](/images/Flask%20Cheat%20Sheet.webp)

---

### Table of Contents

- [Flask Cheat Sheet](#flask-cheat-sheet)
  - [**1. Basic Setup**](#1-basic-setup)
  - [**2. Routing**](#2-routing)
  - [**3. HTTP Methods**](#3-http-methods)
  - [**4. Rendering Templates**](#4-rendering-templates)
  - [**5. Working with Forms**](#5-working-with-forms)
  - [**6. Redirects and URL Building**](#6-redirects-and-url-building)
  - [**7. Static Files**](#7-static-files)
  - [**8. Session Management**](#8-session-management)
  - [**9. Error Handling**](#9-error-handling)
  - [**10. JSON Responses**](#10-json-responses)
  - [**11. Flask Extensions**](#11-flask-extensions)
  - [**12. Running the App**](#12-running-the-app)

## Flask Cheat Sheet

### **1. Basic Setup**

```python
# Install Flask
pip install flask

# Create a basic Flask app
from flask import Flask
app = Flask(__name__)

@app.route('/')
def home():
    return "Hello, Flask!"

if __name__ == '__main__':
    app.run(debug=True)
```

### **2. Routing**

```python
# Route with a variable
@app.route('/user/<username>')
def show_user_profile(username):
    return f"User: {username}"

# Route with an integer variable
@app.route('/post/<int:post_id>')
def show_post(post_id):
    return f"Post ID: {post_id}"
```

### **3. HTTP Methods**

```python
# Handling different HTTP methods
@app.route('/login', methods=['GET', 'POST'])
def login():
    if request.method == 'POST':
        return "Handling POST request"
    else:
        return "Handling GET request"
```

### **4. Rendering Templates**

```python
from flask import render_template

@app.route('/hello/<name>')
def hello(name):
    return render_template('hello.html', name=name)
```

```html
<!-- hello.html -->
<!doctype html>
<html>
  <body>
    <h1>Hello, {{ name }}!</h1>
  </body>
</html>
```

### **5. Working with Forms**

```python
from flask import request

@app.route('/submit', methods=['POST'])
def submit():
    username = request.form['username']
    return f"Submitted username: {username}"
```

```html
<!-- form.html -->
<form action="/submit" method="POST">
  <input type="text" name="username">
  <input type="submit">
</form>
```

### **6. Redirects and URL Building**

```python
from flask import redirect, url_for

@app.route('/admin')
def admin():
    return redirect(url_for('home'))

@app.route('/profile/<username>')
def profile(username):
    return f"Profile page of {username}"
```

### **7. Static Files**

```python
# Serving static files like CSS, JavaScript, or images
url_for('static', filename='style.css')

# In HTML template
<link rel="stylesheet" href="{{ url_for('static', filename='style.css') }}">
```

### **8. Session Management**

```python
from flask import session

# Set a session variable
session['username'] = 'admin'

# Get a session variable
username = session.get('username')

# Clear a session
session.pop('username', None)
```

### **9. Error Handling**

```python
@app.errorhandler(404)
def page_not_found(e):
    return "Page not found!", 404

@app.errorhandler(500)
def internal_server_error(e):
    return "Internal server error", 500
```

### **10. JSON Responses**

```python
from flask import jsonify

@app.route('/data')
def data():
    return jsonify({"name": "John", "age": 30})
```

### **11. Flask Extensions**

```python
# Flask-SQLAlchemy for database integration
from flask_sqlalchemy import SQLAlchemy
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///site.db'
db = SQLAlchemy(app)

# Flask-Migrate for database migrations
from flask_migrate import Migrate
migrate = Migrate(app, db)

# Flask-WTF for form handling
from flask_wtf import FlaskForm
from wtforms import StringField
from wtforms.validators import DataRequired

class MyForm(FlaskForm):
    name = StringField('Name', validators=[DataRequired()])
```

### **12. Running the App**

```bash
# Run the Flask app
export FLASK_APP=app.py
export FLASK_ENV=development
flask run
```

---

This cheat sheet covers the basics of Flask, but Flask has many more capabilities that can be explored through its [official documentation](https://flask.palletsprojects.com/).
