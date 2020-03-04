# Flask + gunicorn WSGI + flask-restx
Some info extracted from this post: https://camillovisini.com/barebone-flask-rest-api-on-aws-elastic-beanstalk/

Flask-restx is the maintained version of flask-restplus (flask-restplus is not maintained anymore!). Check github for more info: https://github.com/noirbizarre/flask-restplus

wsgi.py file is used by gunicorn.

app.py file is changed to be used with restx

#Run
First option: Run with python interpreter (only for debugging)
````
python3 app.py --debug
````

Second option: Run with gunicorn (used for production later)
````
gunicorn --bind 0.0.0.0:8080 wsgi:application -w 1
````
