## Docker

- With Docker it doesn’t matter if you are using a Mac, Windows, or Linux computer anymore. The entire development environment is isolated: programming language, software packages, databases, and more.

- Virtual environments can only isolate Python packages. They still rely on a global, system-level installation of Python albeit they can refer to the proper version. So when we use Python 2.7 in a project, we’re pointing to an installation of Python 2.7 on the computer itself, not actually within the virtual environment.

- Also we can’t run a production database or other services within virtual environments so compared to Docker containers they are far more limited.

### Install Docker

- To install Docker we need to download the desktop app on our computer and create a free account. 

- **Docker Compose** is an additional tool that is automatically included with Mac and Windows downloads of Docker. However if you are on Linux, you will need to add it manually. You can do this by running the command `sudo pip install docker-compose` after your Docker installation is complete.

- To confirm Docker installed correctly we can run our first command `docker run hello-world`. This will download an official image and then run the container.

### Images and Containers
- Images and containers are the two fundamental concepts to grasp when you start with Docker.
    - An **image** is a snapshot in time of what a project contains.
    - A **container** is a running instance of the image.

- When we ran `hello-world` we used an official Docker image. We did not have to create the image ourself. But typically we will create custom images and we do so using a **Dockerfile**. We also will use **docker-compose.yml** files to run the containers.

![](https://techviewleo.com/wp-content/uploads/2021/01/container-architecture-components.png)


## Django REST Framework

![](https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/11/django-rest-framework-2.jpg)


- Django REST Framework is added just like any other third-party app. Add the `djangorestframework` library

- Add it to the INSTALLED_APPS config in our settings.py file

- Ultimately, our API will expose a single endpoint that lists out all books in JSON. So we will need a new URL route, a new view, and a new serializer file.

- There are multiple ways we can organize these files however my preferred approach is to create a dedicated api app. That way even if we add more apps in the future, each app can contain the models, views, templates, and urls needed for dedicated webpages, but all API-specific files for the entire project will live in a dedicated api app.