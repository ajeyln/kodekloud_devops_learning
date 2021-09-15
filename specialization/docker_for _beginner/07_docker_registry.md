<h1 align="center"> Docker Registry </h1>

## Docker Registry

The Centrl repository, where all Docker images are store are called Docker Registry.

when we create a container with an image naming convention, we need to use pattern <br />
``` docker run <DNS NAME>/ <User /Account Name>/<Image/repository>``` <br />
	* The Default registry is Docker Hub and DNS name of Docker Hub is docker.io 
	* If we are not specified location,the image will be store or pulled from default location.
	* User name is docker hub account name or organization name.
	* If we don't provide user/account name or repository name it assumes that it is that same as the given <br />
		Eg: When we want to create container with Nginx image, we can pull image as 
			```docker run nginx or docker run nginx/nginx```

### Private Registry

When we have application built in-house, That shouldn't be made available to the public, We can host an internal <br/>
private registry. Many cloud service provider such as AWS , Azure provide provide private registry by default.

If we need to access private registry before using the images from it and we can login the registory following the command<br />
```docker login <DNS NAME>```

### Deploy Private Registry

When we want to access our own image on premise or internal network, we can use port number along with localhost <br />
and repository informations <br />
``` docker image  localhost:<port>/ <Image/repository>``` <br />