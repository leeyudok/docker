Docker 에 jenkins 설치하기 -  Mac

docker pull jenkins

docker run --name jenkins -d -p 49001:8080 -v $PWD/Documents/Docker/jenkins:/var/jenkins_home -t jenkins 