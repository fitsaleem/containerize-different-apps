# follow these steps for dockerize your python flask application

# step: 01

***first you need to  create your python app.py application***

**after that creat the docker**

***Here's an example Dockerfile for a Python Flask app:***

```
FROM ubuntu

RUN apt-get update
RUN apt-get install -y python3 python3-pip
RUN pip install flask

COPY app.py /opt/app.py

ENTRYPOINT FLASK_APP=/opt/app.py flask run --host=0.0.0.0
```
# step: 02 build the image

Flask app is contained in a file named app.py in the same directory as your Dockerfile, you can build and run the container with the following commands:

```
docker build -t my-flask-app .
docker run -p 5000:5000 my-flask-app
```

This will expose the Flask app on port 5000 in the container and map it to port 5000 on your local machine, so you can access it in your web browser at http://localhost:5000.
