# Installing Jenkins on MacOSX
1. docker build -t myjenkins-blueocean:2.440.1-1 .
2. docker network create jenkins
3. docker network ls
4. docker images
5. docker rmi <iamge_ID>
6. $docker run --name jenkins-blueocean --restart=on-failure --detach --publish 8080:8080 --publish 50000:50000 myjenkins-blueocean:2.440.1-1
7. docker stop -f image_id # force stop
8. docker ps
9. docker exec jenkins-blueocean cat /var/jenkins_home/secrets/initialAdminPassword # get the administrator password for http://localhost:8080/
