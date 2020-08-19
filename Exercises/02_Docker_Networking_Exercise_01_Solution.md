# Assignment: DNS Round Robin Test
***
In this assignment you will use multiple created networks to respond to one DNS address. 

0. Create a docker network 'msi'
1. Create two Elastic Search Containers from the Image ```elasticsearch:2```
2. Make sure when creating the images to use the option ```–network-alias search``` to give the containers an additional DNS name to respond to
3. Run a (adhoc) container from an alpine image with the command ```nslookup``` to verify the ip addresses that respond to the alias ```search``` in the network created above ```msi```by combining both: ```search.msi```
4. Run a container from a centos image with the command ```curl –s search.msi:9200``` on the msi network and monitor whether the output changes (check "name", Elasticsearch names itsself differently whenever a container is started) everytime you rerun the container.  
***
# Solution to Assignment
Create a network named msi and run or more elastic search containers with a network-alias named search 
```
docker network create msi
```
```
docker container run –d -–net msi -–net-alias search elasticsearch:2
```
```
docker container ls
```
```
docker container run --rm --net=msi alpine nslookup search
```
```
docker container run --rm --net=msi centos curl -s search:9200/_cat/health
```
```
docker container ls
```

