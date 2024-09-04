# Flask Cheat Sheet
Here’s a basic cheat sheet for Flask, a popular Python web framework.

### Table of Contents

- [**Setup**](#setup)
- [**Routing**](#routing)
- [**Request and Response**](#request-and-response)
- [**Templates**](#templates)
- [**Static Files**](#static-files)
- [**Blueprints**](#blueprints)
- [**Error Handling**](#error-handling)
- [**Sessions**](#sessions)
- [**Debugging**](#debugging)

---

### Setup

1. **Install Flask**:
   ```bash
   pip install Flask
   ```

2. **Basic Application**:
   ```python
   from flask import Flask

   app = Flask(__name__)

   @app.route('/')
   def home():
       return 'Hello, World!'

   if __name__ == '__main__':
       app.run(debug=True)
   ```

### Routing

- **Basic Route**:
  ```python
  @app.route('/path')
  def function_name():
      return 'Response'
  ```

- **Dynamic Routes**:
  ```python
  @app.route('/user/<username>')
  def show_user_profile(username):
      return f'User {username}'
  ```

- **HTTP Methods**:
  ```python
  @app.route('/post', methods=['POST'])
  def handle_post():
      return 'POST request'
  ```

### Request and Response

- **Access Request Data**:
  ```python
  from flask import request

  @app.route('/form', methods=['POST'])
  def form():
      username = request.form['username']
      return f'Hello {username}'
  ```

- **JSON Request**:
  ```python
  @app.route('/json', methods=['POST'])
  def json_example():
      data = request.json
      return f"Received data: {data}"
  ```

- **Response Object**:
  ```python
  from flask import make_response

  @app.route('/response')
  def custom_response():
      response = make_response('Custom response')
      response.headers['X-Custom-Header'] = 'Value'
      return response
  ```

### Templates

- **Render Template**:
  ```python
  from flask import render_template

  @app.route('/hello')
  def hello():
      return render_template('hello.html', name='World')
  ```

  In `templates/hello.html`:
  ```html
  <!doctype html>
  <html>
      <head><title>Hello</title></head>
      <body>
          <h1>Hello {{ name }}!</h1>
      </body>
  </html>
  ```

### Static Files

- **Serve Static Files**:
  - Place static files (CSS, JS) in a folder named `static`.
  - Access static files via `/static/filename`.

### Blueprints

- **Create and Register Blueprint**:
  ```python
  from flask import Blueprint

  example_bp = Blueprint('example', __name__)

  @example_bp.route('/example')
  def example():
      return 'Blueprint example'

  app.register_blueprint(example_bp)
  ```

### Error Handling

- **Custom Error Pages**:
  ```python
  @app.errorhandler(404)
  def not_found_error(error):
      return 'Page not found', 404

  @app.errorhandler(500)
  def internal_error(error):
      return 'Internal server error', 500
  ```

### Sessions

- **Using Sessions**:
  ```python
  from flask import session

  app.secret_key = 'supersecretkey'

  @app.route('/set_session')
  def set_session():
      session['username'] = 'admin'
      return 'Session data set'

  @app.route('/get_session')
  def get_session():
      username = session.get('username', 'not set')
      return f'Username is {username}'
  ```

### Debugging

- **Enable Debug Mode**:
  ```python
  if __name__ == '__main__':
      app.run(debug=True)
  ```

This cheat sheet covers the basics of Flask, but Flask has many more capabilities that can be explored through its [official documentation](https://flask.palletsprojects.com/).
