# docker-sample
essai dockerfile

apt update
apt -y install python3 python3-pip nano
pip3 install flask
touch /opt/app.py

```
# app.py
import os
from flask import Flask
app = Flask(__name__)
@app.route("/")
def main():
    return "Welcome!"
@app.route('/how are you')
def hello():
    return 'I am good, how about you?'
if __name__ == "__main__":
    app.run()
```

```
FLASK_APP=/opt/app.py flask run --host=0.0.0.0
```
