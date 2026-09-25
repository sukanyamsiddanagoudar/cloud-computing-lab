# Experiment 1: Containerize and Run a Simple Python Web Application

## Objective

To containerize and run a simple Python Flask web application using Docker.

## Technologies Used

* Python
* Flask
* Docker
* Docker Desktop

## Project Structure

```text
Docker-Python-App/
├── Dockerfile
├── app.py
├── requirements.txt
├── README.md
└── screenshots/
```

## Application

The Flask application displays:

```text
Hello! My first Docker application is running.
```

The application runs on port **5000**.

## Dockerfile

The Dockerfile:

* Uses Python 3.12
* Creates the working directory
* Installs Flask
* Copies the application
* Exposes port 5000
* Runs the Flask application

## Main Docker Commands

```powershell
docker --version
docker run hello-world

docker build -t my-python-app .
docker images

docker run -d -p 5000:5000 --name my-python-container my-python-app
docker ps

docker logs my-python-container

docker stop my-python-container
docker start my-python-container

docker rm my-python-container
docker ps -a
```

## Working

```text
Flask Application
       ↓
   Dockerfile
       ↓
  Docker Image
 my-python-app
       ↓
Docker Container
my-python-container
       ↓
 http://localhost:5000
```


## Result

The Python Flask application was successfully containerized and run using Docker. The application was accessed through the browser, and Docker container operations such as logs, stop, start, and removal were successfully performed.
