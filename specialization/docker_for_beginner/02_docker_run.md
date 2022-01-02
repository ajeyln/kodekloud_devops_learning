<h1 align="center"> Docker run commands (Advanced) </h1>

The following are the advanced Docker run commands used for operations

| Commands | Description | 
|---------|--------------|
| docker run < IMAGE >:< TAG > | is used to run a container with specified version mentioned in Tag|
| docker run -it < IMAGE >| the docker will prompt the standard input from terminal| 
| docker run -p < LATEST PORT >:< CURRENT PORT > < IMAGE >| to assign the container to latest port | 
| docker run -v < EXTERNAL DIRECTORY >:< INTERNAL DIRECTORY > < IMAGE > | to mapping for persists / save the data on external directory   |
| docker inspect < CONTAINER - ID > | to get information about container in json format|
| docker logs < CONTAINER - ID > | to get log information about container|


### Labs

1. Docker run commands 