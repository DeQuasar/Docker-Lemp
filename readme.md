# Simple Docker Lemp Stack
This is a **simple** development environment running the **LEMP Stack** (Linux, Nginx, MariaDB, PHP7.1). 
This docker environment is in no way intended to be used in production for the time being. 

Folder Structure
------

- **Docker** - Holds all the docker-compose files
    - **Nginx**  
        - **Conf** - Nginx configuration files
        - **Logs**
            - **Access.log** - Nginx access log
            - **Error.log** - Nginx error log
    - **PHP**
        - **Conf** - PHP configuration files        
- **Public** - Application web root 

Services
------
> Nginx - PHP7.1 - MariaDB - PHPMyAdmin

* Nginx
    * Address - Localhost or Hostfile equivalent
    * Ports - 80 and 443
* PHP
    * Version 7.1
* MySQL
    * Address - Localhost
    * Ports - 3306
    * Environment Variables
        * Root Password - root 
* PHPMyAdmin
    * Address - Localhost:8080
    * Ports - 8080
        * Environment Variables
            * Host - mariadb
            * Username - root
            * password - root
    



Usage Instructions
------

All commands will be executed in the **folder** where the **docker-compose.yml** is located

#### Start the server
> docker-compose up -d

#### Stop the server
> docker-compose down

#### Kill the containers
> docker-compose kill

TODO
------
Add PHP Configuration files (php.ini, php-fpm)
Add SSL support

Issues, Questions, Concerns
------
If you have any issues, questions, or concerns please open up an issue and I will get back to you.