# Docker

<pre><code>
https://docs.docker.com/engine/getstarted/step_six/
</code></pre>


<pre><code>
docker pull jenkins

docker run --name jenkins -d -p 48080:8080 -v $PWD/Documents/Docker/jenkins:/var/jenkins_home -t jenkins 

http://192.168.99.100:48080
</code></pre>