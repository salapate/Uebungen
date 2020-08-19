# Assignment: Developing a website using bind mounts
This assignement is to show how developers can use bind mounts to leverage easy development. A bind mount will be set up. At the same time an app will be instanciated on an nginx webserver via a container.  You as a developer need to change a few things before you can show the web page to your customer. Your container has all the tools required to facilitate your development. The following changes need to be accomplished

#### Please Perform the following: 
1. You will need to set up a neccessary bind mount thereby linking it to the cafe folder in your repository
2. Change the Address on line 261 from „4578 Marmora Road, Glasgow DA04 89GR” to “Berlin-Wilmersdorf Uhlandstr 20, DE 10719
3. Change the Phone No. on line 262 From “800 2345-6789” to “+49 30 577 88 94”
4. Change the Phrase “Welcome” on line 113 to “We welcome you to our place”

#### To accomplish this exercise 
1. You will use Visual Studio Code
2. You will find the neccessary files within the 05_2_dockerfile-sample-2/cafe folder 
3. You will need to understand what the defined WORKDIR is

##### The changes II, III and IV will be done via a code editor Visual Studio Code
***
# Solution to Assignment
#### 1. Find out how to set up a bind mount
<-- docker run --name some-nginx -v /some/content:/usr/share/nginx/html -d nginx 
You will find this information on the docker hub/official nginx image, how to bind mounts-->


#### 2. Navigate to the file where the static data is to be found

```
cd to /Uebungen/08_Data_Management/Data/cafe
```

#### 3. Instanciate the Docker Container make sure 

```
docker run -p 8090:80 --name nginx-webserver -v /home/km/Kurs/08_Data_Management/Data/cafe:/usr/share/nginx/html -d nginx
```
#### 4. Open your web browser and navigate

```
http://localhost:8090

```
#### 5. Open the file **index.html** with the Visual Studio Code Editor and perform the following changes:
```
* line 261: Change the Address from „4578 Marmora Road, Glasgow DA04 89GR” to “Berlin-Wilmersdorf Uhlandstr 20, DE 10719​
* line 262: Change the Phone No. from “800 2345-6789” to “+49 30 577 88 94”​
* line: 113: Change the Phrase “Welcome” to “We welcome you to our place”
```
<--After every change we need not rebuild the image everytime -->
