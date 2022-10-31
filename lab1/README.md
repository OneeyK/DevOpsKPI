Create a json file with all dependencies and installing it
>> nano package.json
>> npm install
Creating our easy server
>> nano server.js
Creating a docker file
>> nano Dockerfile
Building our docker image
>> docker build -t webapp:v1 .
Running our image on port 80 with memory and cpu limits
>> docker run -p 80:80 -d --name webapp -m 1024m --cpus="1.5" webapp:v1
