# Flask + gunicorn WSGI + flask-restx
Some info extracted from this post: https://camillovisini.com/barebone-flask-rest-api-on-aws-elastic-beanstalk/

Flask-restx is the maintained version of flask-RESTPLUS (this is not being maintained anymore!)

wsgi.py file is used by gunicorn.

#Run
First option: Run with python interpreter (only for debugging)
````
python3 app.py --debug
````

Second option: Run with gunicorn (used for production later)
````
gunicorn --bind 0.0.0.0:8080 wsgi:application -w 1
````
