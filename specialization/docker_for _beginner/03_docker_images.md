<h1 align="center"> Docker Images </h1>

## Docker Images

A Docker Image is a template that contains the application, and all the dependencies required to run that application on Docker. 

### Creating our own Images

We can customize the docker images using the dockerfile and make it available on Docker Hub registry after customization using command

```docker push <DockerHub address>```

### Dockerfile

A Dockerfile is a text document that written in instruction and argument format that docker can understand.

	+ Instruction will instruct the Docker to perform a specific action while creating the image and it should be written <br />
	on left side of docker file in Capital Letters. <br />
	+ Arguments are the arguments for the instruction specified in Dockerfile.
	
we can build an image using the docker file using command

```docker build dockerfile -t <Customized image>```

A sample dockerfile is created to build image of web server using flask command as an Example

```dockerfile

FROM Ubuntu # base OS of the countainer

RUN apt-get update  # install all dependencies
RUN apt-get install python

RUN pip install flask
RUN pip install flask-mysql

COPY . /opt/source-code # Copy source code

ENTRYPOINT FLASK_APP=/opt/source-code/app.py flask  run  # Specify entrypoint
```

### Layered Architecture

When docker builds an image, it builds the layered architecture, i.e each line of instruction will create a new layer <br />
in the docker image with just the changes from the previous layer. If any case the layer fails or if we want to add any steps <br />
in build process, the layer architecture will help us to restart the docker build from the particular layer were it failed.

Eg:
```dockerfile

FROM Ubuntu 

RUN apt-get update 
RUN apt-get install python

RUN pip install flask
RUN pip install flask-mysql

COPY . /opt/source-code 

ENTRYPOINT FLASK_APP=/opt/source-code/app.py flask  run
```

In the above example the docker will create layer as follows (these information is available in build command):<br />
	* Layer 1 - Base Ubuntu OS layer
	* Layer 2 - Changes in apt packages
	* Layer 3 - Changes in pip packages
	* Layer 4 - Source Code
	* Layer 5 - Update Entrypoint with "flask" command

We can check the layer with size information for each layer using the command
``` docker history <dockerfile_name>```

### Enviornment variable in Docker image

If we want to change any feature in application code like font,size,background etc., We can set an enviornment variable while running container <br />
to avoid to make often changes in application code.

``` docker run -e APP_COLOR=<COLOR> <IMAGE-NAME>```

we can check the enviornment variable on running container using
``` docker inspect <IMAGE-NAME>```

### Labs

1. Docker Images - Creating docker file 
2.  Enviornment Varioable - Setup 