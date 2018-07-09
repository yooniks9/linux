## Dockers Command 

##### show all dockers
```docker ps -a```
##### stop single docker's container
```docker stop CONTAINER-ID```
##### stop all docker's containers
```docker stop $(docker ps -a -q)```
##### remove single docker's container
```docker rm CONTAINER-ID```
##### remove all dockers
```docker rm $(docker ps -a -q)```
##### show all downloaded docker images
```docker images```
##### remove single docker's images
```docker rmi IMAGE-ID```
##### remove all docker's images
```docker rmi $(docker images)```
##### get docker IP address
```docker inspect CONTAINER-ID | grep "IPAddress" ```
##### SSH to docker 
```docker exec -it CONTAINER-ID bash ```
##### Execute PHP inside docker
```docker exec CONTAINER-ID /usr/local/bin/php /var/www/html/artisan october:env ```
##### MySQL backup - Execute MySQLdump inside docker
```docker exec -it CONTAINER-ID  /usr/bin/mysqldump -u$USERNAME --password=$PASSWORD $DBNAME > backup.sql ```
##### MySQL Restore - Restore MySQL Data into docker
```cat backup.sql | docker exec -i CONTAINER /usr/bin/mysql -u$USERNAME --password=$PASSWORD $DBNAME```
##### clean docker sync cache [read-more](https://github.com/EugenMayer/docker-sync/wiki)
```docker-sync clean```
##### Due to file system issues, docker mount are extremely slow on MacOS / Windows, We need to host the File services with Unison
```docker-sync start```
##### Start Docker-compose
```docker-compose up -d```
##### Start Docker-compose with specify config file other than docker-compose.yml
```docker-compose -f docker-compose-prod.yml up -d```