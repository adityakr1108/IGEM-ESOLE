from flask import Flask, render_template
import time
from os import path
from pathlib import Path
from flask_frozen import Freezer  # Update this line

# Set up paths
static_folder_path = path.abspath('./static')
template_folder_path = path.abspath('./wiki')
app = Flask(__name__, static_folder=static_folder_path, template_folder=template_folder_path)

# Flask-Frozen Configuration
app.config['FREEZER_DESTINATION'] = 'public'
app.config['FREEZER_RELATIVE_URLS'] = True
app.config['FREEZER_IGNORE_MIMETYPE_WARNINGS'] = True
freezer = Freezer(app)

@app.cli.command()
def freeze():
    """Command to freeze the app"""
    freezer.freeze()

@app.cli.command()
def serve():
    """Command to serve the frozen pages"""
    freezer.run()

@app.after_request
def add_header(response):
    # Disable caching for development
    response.cache_control.no_cache = True
    response.cache_control.no_store = True
    response.cache_control.max_age = 0
    response.cache_control.public = False
    return response

@app.route('/')
def home():
    current_time = int(time.time())
    return render_template('pages/home.html', current_time=current_time)

@app.route('/<page>')
def pages(page):
    current_time = int(time.time())
    return render_template(f'pages/{page.lower()}.html', current_time=current_time)

if __name__ == "__main__":
    app.run(port=8000, debug=True)
