Step 1: Install Docker 
sudo apt update 
sudo apt install docker.io -y 
 
Step 2: Verify Docker Installation 
docker --version 
 
Step 3: Create HTML File (index.html) 
<html> 
<head> 
    <title>Docker Practical</title> 
Page 32 of 33 
 
</head> 
<body> 
    <h1>Welcome to Docker Container</h1> 
    <h2>Version Control using Git</h2> 
</body> 
</html> 
Give feedback 
 
Step 4: Create Dockerfile 
FROM nginx:latest 
COPY index.html /usr/share/nginx/html/index.html 
EXPOSE 80 
 
Step 5: Build Docker Image 
docker build -t simple-webapp . 
 
Step 6: Run Docker Container 
docker run -d -p 8080:80 simple-webapp 
