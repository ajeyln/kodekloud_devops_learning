<h1 align="center"> Web Server </h1>

### Standalone vs Client based Application

+ **Standalone application** : It is application that carrys out certain task or operations on a stand alone <br />
local computer. All logic is built inside the application and it doesn't need to make any external communication.

+ **Client based application** : A software installed on client machine acting as user interface and interact <br />
with specific server. 

### Web FrameWorks & Web Servers

The client sends a request to the server and the server returns a response.  

+ **Backend (Server-side) code** : It is a set of the code that runs on the server side that is actually hosting the web server <br />
 and the code that's listening for connection from user and querying database. 

+ **Frontend Code** : The reponse sent back by the server could be another set of code that runs on the client side that is used <br />
to display webpages and information within pages.

Websites are brodly classified into two types

* **Static Websites** : A website that only use HTML pages, some CSS styling and images such as a websites that shows a list of pictures <br />
as an image gallery could be classified as static website. There is no interaction with the server after the content is served.

* **Dynamic Websites** : These websites usually require both static and dynamic content. A information about products are retrieved <br/>
from the database before displaying them on the webpage. These webpages displayed differently based on the data in the database.

#### Apache Web Server

It is web server is used to serve web content like HTML, CSS and javascript file and 80 is default port for Apache Web Server.

Step to install Apache Web Server on Centos

* yum install httpd : install apache webser
* service httpd start : start the httpd(apache server)
* cat /var/log/httpd/access_log : Access logs are updated whenever a user access the websites.
* cat /var/log/httpd/error_log : These logs are updated whenever there is an error.
* /etc/httpd/conf/httpd.conf : Configuration files which is configured the different parameters that govern how the servers operates.
* service restart httpd : restart the httpd after configuration has been changed.

#### Apache Tomcat

Apache Tomcat server provides a web server environment where we can host Java-based web application and 8080 is default port of Tomcat.

#### Python - Deploy Flask App

1. Flask webserver listening on localhost at certain specified port for user requests <Br />
2. Endpoints <Br />
    * / or /home - renders index.html, homepage of the temple with images and useful links <Br />
    * /register - user can register here  <Br />
        - GET method - form for registration gets displayed <Br />
	    - PUT/POST method - user values for registration will be accepted by server <Br />
    * /update <Br />
        - GET method - for changing user information of existing registered users, here a webpage must be rendered <Br />
        - POST method  -  user values to be sent to flask for updation <Br />
    * /delete <Br />
        - GET Method - a form for deleting user <Br />
        - POST method - user request must be sent to flask for deletion <Br />
    * /list - renders dynamic webpgae of list of registered users <Br />
    * /statistic <Br />
        - GET Method - a form for statistical informations on users details <Br />
        - POST method - user request must be sent to flask to generate graphs <Br />
    * /contact - renders contact.html, contact information of temple <Br />
    * /* - any other endpoints will display error.html

#### NodeJS - Deploy Express App

Express.js is web framework for Node.js and this application serves some static files located in the public directory  <br />
and some api such as products api to get list of products and it listens on port 3000.

* npm install : It retrieves the list of dependencies and install them.
* node app.js : to run the application code.
* node run start : runs the start scripts which actually runs the particular command.


### Labs

 1. Apache Web Servers : Insllation, info about logs, working on conf files etc.
 2. Flask : Downloading and deployment of flask in python.
 3. NodeJS deploy Express App : installation of dependencies, run the application background etc.
 
 
