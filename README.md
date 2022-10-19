# sampleDockerBuild
This is an example of sample docker image build. It uses the nginx docker images and deploy cafe app in nginx web server.

# Getting Started
1. Clone the repo
```shell
git clone https://github.com/vinaykagithapu/sampleDockerBuild.git
cd sampleDockerBuild
```
2. Build a cafe web application docker image.
```shell
docker build -t cafe-webapp .
docker images
```
3. Run cafe web application container.
```shell
docker run --name=cafe-app -it -dp 8083:80 cafe-webapp 
```
4. Vist the cafe web application at http://localhost:8083

# CleanUp
```shell
docker stop cafe-app
docker rm cafe-app
docker rmi cafe-webapp:latest
```