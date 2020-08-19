# Assignment: CLI App Testing
***
Imagine yourself a Systemadministrator who gets a ticket to check the versions of curl installed on a CentOS 7 and Ubuntu 14.04. The commads you may need to accomplish this task,  you will find below.

* Use different Linux distro containers to check ```curl``` cli tool version
* Use two different terminal windows to start bash in both ```centos:7``` and ```ubuntu:14.04```, using ```-it```
* Learn the ```docker container run —rm``` option so you can save cleanup
* Ensure ```curl``` is installed and on latest version for that distro
* ubuntu: ```apt-get update && apt-get install curl```
* centos: ```yum update curl```
* Check ```curl --version```