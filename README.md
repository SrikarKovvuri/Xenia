Xenia Flutter Web App in Docker
This repository contains a Flutter web application configured to run in a Docker container. Follow the steps below to build and run the application locally.

Prerequisites
Docker: Make sure Docker is installed and running on your system. You can download Docker here.

1. Clone the Repository
Clone the repository to your local machine:



git clone https://github.com/your-username/xenia_flutter_app.git
cd xenia_flutter_app

2. Build the Docker Image
In the project directory, build the Docker image using the following command:



docker build -t flutter-app .
3. Run the Docker Container
Once the image is built, run a container using this command:



docker run -p 8080:8080 flutter-app

This command maps port 8080 inside the Docker container to port 8080 on your local machine.

4. Access the Application
Open a web browser and navigate to:

http://localhost:8080