Docker
 
 Docker is software development platform
 Here you packaged app in images
 Container use image to start application
 Containers run on any operating system
 It works exactly same independent of OS, machine, Environment
 Lightweight compared to VM
 Easier to maintain & deploy
 Docker works with any language, runtime, OS

Demo : Create a Simple python webapp on Cloudshell
1  gcloud config set project snappy-benefit-421114

2  python3

3  nano main.py

    
    from flask import Flask

    app = Flask(__name__)


    @app.route('/')
    def index():
    return 'Welcome to Python Flask World v2.0'


    if __name__ == '__main__':
    app.run(host='0.0.0.0', port=8080)


 4  ls
 
 5  python3 main.py

 CREATE A DOCKERFILE
   gcloud config set project snappy-benefit-421114
   ls
   docker
   docker version
   mkdir devops
   cd devops/
   mkdir docker-basics
   cp main.py devops/docker-basics/
   cd devops/docker-basics/   

STEPS
   BASE IMAGE-linux
   python
   install flask
   start flask web app

   hostport:containerport
   9090:8080

   
 CODE
   FROM python: 3.10-slim
   RUN pip install flask
   WORKDIR /myapp
   COPY main.py /myapp/main.py
   CMD ["python", "/myapp/main.py"]

 COMMANDS
 
 gcloud config set project snappy-benefit-421114
  
     cd devops
     cd docker-basics
     ls
     docker build -t gcr.io/gcp-devops-338510/myfimage:v1.0 .
     nano Dockerfile
     docker build -t gcr.io/gcp-devops-338510/myfimage:v1.0 .
     docker images
    cd Dockerfile
    ls
    docker pull hello-world
    docker run hello-world
    docker images
    docker run -p 9090:8080 gcr.io/gcp-devops-338510/myfimage:v1.0
     docker ps -a
     docker rm <containerid>
     
