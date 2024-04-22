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
    


    https://8080-cs-187d79a5-c3ba-47c8-a4e4-0a15b7e9d1d4.cs-us-east1-pkhd.cloudshell.dev/?authuser=0&redirectedPreviously=true

    Welcome to Python Flask World v2.0
   
