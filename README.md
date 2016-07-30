# Docker

## getstarted
<pre><code>
(https://docs.docker.com/engine/getstarted/step_six/)
</code></pre>

## Docker: Remove all images and containers

<pre><code>
#!/bin/bash
# Delete all containers
docker rm $(docker ps -a -q)
# Delete all images
docker rmi $(docker images -q)
</code></pre>

## Installing Tomcat with Docker
<pre><code>
docker pull leeyudok/tomcat

docker run --name tomcat -d -p 48090:8080 -t leeyudok/tomcat 

http://192.168.99.100:48090
</code></pre>


## Jenkins

### Installing Jenkins with Docker
<pre><code>
docker pull leeyudok/jenkins

docker run --name jenkins -d -p 48080:8080 -v $PWD/Documents/Docker/jenkins:/var/jenkins_home -t leeyudok/jenkins 

http://192.168.99.100:48080
</code></pre>

### Addtionally, you can configure nginx as a reverse proxy to your Jenkins instance, e.g.
<pre><code>
upstream app {
    server 127.0.0.1:49001;
}
server {
    listen 80;
    server_name jenkins.your-domain.com;

    location / {
        proxy_pass http://app;
    }
}
</code></pre>