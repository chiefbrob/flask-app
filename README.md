# Learning Flask
This is a simple repo where I will create a simple blog with Flask

## Getting Started

First we create a Virtual Environment (venv)

`python3 -m venv blog`

`cd blog`

Next we activate

`source bin/activate`

Install Flask

`pip install flask`

Verify Installation

`python -c "import flask; print(flask.__version__)"`

Create `index.py` 

```python
from flask import Flask, render_template

app = Flask(__name__)


@app.route('/')
def hello():
    return 'Hello, World!'

@app.route(‘/about’)
def about():
    return render_template('about.html')
```

Create about page file

`nano templates/about.html`

`export FLASK_APP=index`

`export FLASK_ENV=development`

`flask run -p 8080`
