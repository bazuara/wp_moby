# wp_moby

This is a small compose file, deploying and configuring Wordpress, MySQL and phpMyAdmin, with persistency. 
It creates an internal network to connect services, no need to redirect traffic, except behind an external nginx service.


## Ports and folders


| Service |External port| Internal port|
|--|--|--|
|Wordpress page|8000|80|
|phpMyAdmin| 8080 | 80 |
|mySQL| - | 3306|


## Files and folders

|File/Folder| content|
|--|--|
|.env|Stores passwords for installation. Copy *.env.example* and edit with your desired configuration.|
|wp_files| Contains all internal files related to the Wordpress site deployed.|
|db_data | Contains databases for mySQL process. Just for persistency. |

 
## Installation and run

```git clone https://github.com/bazuara/wp_moby.git && cd wp_moby && docker-compose up -d ```

## Stop

``` docker-compose stop 

