# 5007-Tutorial5 Hotel California International Waitlist System
#### Name: Liu Linxi  
#### Student Number:A0228591X

## Part I: Environment Setup
#### 1. ubuntu 
```
docker pull ubuntu
```
#### 2. run the container with port 3000 and port 5000 
```
docker run -p 3000:3000 -p 5000:5000 -dit ubuntu
```
#### 3. install nvm and npm
```
apt update
```
```
apt install curl
```
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
``` 
#### 4. restart the container and do the following
```
nvm install 10
```
```
npm install -g npm@6
```

#### 5. mongodb installation
```
apt install gnupg
```
```
apt install curl
```
```
curl -fsSL https://www.mongodb.org/static/pgp/server-4.4.asc | apt-key add -
```
```
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.4 multiverse" | tee /etc/apt/sources.list.d/mongodb-org-4.4.list 
```
```
apt update
```
```
apt install mongodb-org
```
```
apt install screen
```
```
mkdir -p /data/db
```
```
screen mongod
```
###### press Ctrl+a followed by d to return to terminal

#### 6. git installation and clone
```
apt install git
```
```
git clone https://github.com
```

## Part II : Commands 
#### 1. dependencies installation
```
cd api
```
```
npm install
```
```
cd ../ui
```
```
npm install
```
```
cd ..
```
#### 2. start the mongodb
```
screen mongod
```
###### Press Ctrl+a followed by d to return to terminal


#### 3. initialize the database and run the back-end api [in folder "api"]
```
mongo issuetracker scripts/init.mongo.js
```
```
screen npm start
```
###### Press Ctrl+a followed by d to return to terminal
#### 4. run the front-end ui [in folder "ui"]
```
cd ../ui
```
```
screen npm start
```
###### Press Ctrl+a followed by d to return to terminal   
#### 5. view the app from browser
##### open **`localhost:3000`** in your browser 
  
