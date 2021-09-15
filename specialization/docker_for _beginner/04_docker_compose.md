<h1 align="center"> Docker Compose </h1>

### Docker Compose

In docker compose , we can create a configuration file in Ymal format( docker-compose.ymal) and to put together the different services and the options <br />
specific to those to running them in file.

	* If we need to set up a complex  application running multiple services a better way to do it using docker compose.
	* To bring up the application stack using ```docker compose up```
	* Link(--link) is a command line options which can be used to link two containers together

Eg: A sample comands for containers for simple voting application in docker

``` docker-compose.ymal
docker run -d --name=redis redis # container contains redis image for in-memory DB
docker run -d --name=db postgres # container contains redis image for DB
docker run -d --name=vote -p 5000:80 --link redis:redis voting-app # container contains python script for voting app
docker run -d --name=result -p 5001:80 --link db:db result-app # container contains .js script for result
docker run -d --name=worker --link redis:redis --link db:db  worker # container contains worker image for  worker
```
We can write the Docker compose file in ymal file as follows

```
redis:
	image: redis
db:
	image: postgres:9.4
vote:
	image: voting-app
	ports:
		- 5000:80
	links:
		- redis
result:
	image: result-app
	ports:
		- 5001:80
	links:
		- db
worker:
	image: worker
	links:
		- redis
		- db
```

### Docker Compose -  build

If the images are build by us , we can specify image location instead of the name of the image and need to change image to build <br />
so the latest docker-compose file after changes.

```
redis:
	image: redis
db:
	image: postgres:9.4
vote:
	build: ./vote
	ports:
		- 5000:80
	links:
		- redis
result:
	build: ./result
	ports:
		- 5001:80
	links:
		- db
worker:
	build: ./worker
	links:
		- redis
		- db
```

### Docker Compose - version

Docker compose evolved overtime and now supports a lot more options that we did previous.

**version 1 **

The below docker compose is version 1 or original version which has a number of limitation, as if we want to deploy containers on a different <br />
network other than defualt bridged network, It is not possible and the file will say that a dependency on start as the container will start as per the order <br />
mentioned in docker compose not as per the dependencies.

```
redis:
	image: redis
db:
	image: postgres:9.4
vote:
	image: voting-app
	ports:
		- 5000:80
	links:
		- redis
``` 

**version 2**

The below docker compose is version 2,It must indicate the version number at the root of the document. All services must be declared under .<br />
the services key and should specify the version of the docker-compose file at the top of the file as ```version : 2```. In this versioning <br />
system the Docker compose automatically and creates a dedicated network bridged network for the application and then attach all the container<br />
to this new network. Therefore, there is no need to add link option in this version. The version work based on dependencies mentioned  <br />
in compose file and denoted as ```depends_on``` .

```
version : 2
services:
	redis:
		image: redis
	db:
		image: postgres:9.4
	vote:
		image: voting-app
		ports:
			- 5000:80
		depende_on:
			- redis
``` 

**version 3**

The below docker compose is version 3, which is similar as version 2 and should specify the version of the docker-compose file at the top of the <br />
file as ```version : 3```.

```
version : 3
services:
	redis:
		image: redis
	db:
		image: postgres:9.4
	vote:
		image: voting-app
		ports:
			- 5000:80
``` 

### Labs

1. Docker Compose - composing, versioning etc.