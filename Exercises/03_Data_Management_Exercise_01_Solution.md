# Assignment: Update a Postgres database Version 9.6.1 to 9.6.2
##### Find the volume path
Step 1 go to Docker Hub and find the volume path for the postgresql server
[/var/lib/postgresql/data] according to the Dockerfile


##### Start a Docker Container with a named volume psql to sto the data

```
docker container run -d --name psql -v psql:/var/lib/postgresql/data postgres:9.6.1


```
##### Observe the logs for "database is ready to accept connections"

```
docker logs -f psql

```

##### Stop the container 

```
docker container stop psql
```

##### Start a second container with the name psql2 from the updated image postgres:9.6.2

```
docker container run -d --name psql2 -v psql:/var/lib/postgresql/data postgres:9.6.2

```
##### Check the different versions of the containers 

```
docker container ps -a 
```
###### Check the created volume with the created name
```
docker volume ls
```

##### Observe the logs for "database is ready to accept connections"
```
docker container logs -f psql2

``` 
The update has successfully taken place the new version of the postgres:9.6.2 is using the initially created named volume psql




