# Assignment: Minor Database upgarade using Named Volumes 
You need to upgrade your postgresql database from version 9.6.1 to version 9.6.2. At the end of the assignment make sure the data volume used by 9.6.1 is the very same as that which will be used by the version 9.6.2. 

#### To accomplish this exercise 
1. You will need to go to the docker hub to find the standard volume  path of the respective postgresql database (for both versions)
2. Instanciate a postgres:9.6.1 where the name of the container  and the named volume is psql
3. Check if the container has been instanciated appropriately by looking for the following output from the logs: „database system is ready to accept connections"
4. Stop the current psql instance
5. Instanciate a second postgres:9.6.2 with the name psql2, however let it connect to the same psql volume defined before
6. Check if the container has been instanciated appropriately (using the logs) "database system is ready to accept connections"