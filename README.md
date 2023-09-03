# Linux Commands
1. Shell in linux is a CLI that is used to control the OS. eg iterm, terminal in windows, cmd
2. How does os knows the commands like ```git```, ```python3``` etc. They are executable files located in system -> their path is set in the environment variables
3. ```where``` command can be used to find the location of these exec files.
4. List all items in a folder - ```ls``` (list command) (dir in windows)
5. Make Directory - ```mkdir```. Eg creating directory inside a directory -> ```mkdir src/componnts```
6. Making a middle directory between two existing directories. We use-> ```mkdir -p parent_folder/middle_folder/child_folder```
7. Change directory - ```cd```
8. Remove directory - ```rmdir```
9. To reveal a path in file explorer - ```open``` cmd is used (```start .``` in windows)
10. ```ls -a``` -> shows all files including hidden files
11. ```ls -l``` -> detailed information of all the directories
12. ```ls -al``` -> combined command for both.
13. ```ls -R``` ->recursivly lsting all the files.
14. Path variables are stored in the ```zprofiles``` of the zsh cli used by mac
15. ```pwd``` -> print workig directory
16. ```cat``` -> cmd used to print the content of any file eg a js file's code
17. ```cat > hello``` then in next line "my name is Priyansh" -> no such file as hello exists so it gets created with the text contained in it.
18. merging contents of two files one.txt and two.txt -> ```cat one.txt two.txt > new.txt```
19. ```cd .``` will stay in that dir
20. ```cd ..``` will go to previous directory
21. ```man``` command is used to get the deails of a particular command for eg. ```man echo```, this givrs the details of all the information of the ```echo```command
22. ```tr```command is used to Translate the text of a given file to another format. For example to convert text into uppercase: ```cat file.txt | tr a-z A-Z > upper.txt```
23. In the upper example the optput of the first command acts as input for the second command. The Greater than sign ```>``` is for redirection where you the generated output to a particular file.
24. For chaining multiple commands, one after the another you can use ```\``` for the same. Eg ```cat file.txt \ cd ..```
25. Copy command is ```cp```
26. Move command is ```mv```. Eg ```mv file.txt hello``` this will move the file file.txt to the hello directory
27. Using the ```mv``` command we can rename the files as well, for eg. ```mv file.txt hello.txt```
28. Removing a file, we can use the ```rm``` command. For eg ```rm file.txt```
29. 
 
# Docker Concepts

<img src = "https://camo.githubusercontent.com/d51c01c11da6543e620059c21b10a732db3bb9b42f38958ae962e90b8c166402/68747470733a2f2f75706c6f61642e77696b696d656469612e6f72672f77696b6970656469612f636f6d6d6f6e732f372f37392f446f636b65725f253238636f6e7461696e65725f656e67696e652532395f6c6f676f2e706e67">

## Overview

Welcome to the world of Docker! This guide will introduce you to the fundamental concepts and workflows of Docker, a powerful platform for building, running, and shipping applications.

## What is Docker?

**Docker** is a versatile platform that simplifies the development and deployment of applications. It provides a standardized way to package an application and its dependencies into a single, portable unit called a **container**. Here's why Docker is so exciting:

## Key Concepts

1. **Versatility**: Docker allows you to run entirely different applications with unique dependencies on the same system without conflicts. For example, you can run App 1 using Node.js 14 and MongoDB 4 alongside App 2 with Node.js 9 and MongoDB 3.

2. **Isolation**: When you use Docker to build and run an application, it creates an isolated environment. This isolation means that an app can be removed from your system without affecting other apps or their dependencies.

3. **Containers**: Containers are the heart of Docker. They provide a lightweight and consistent environment for running applications.

4. **Virtual Machines (VMs)**: Docker is not to be confused with traditional virtualization technologies. VMs abstract physical hardware, while Docker containers encapsulate applications and their dependencies. For example, on a Mac, you can have Windows and Linux VMs running.

## Advantages of Containers over Virtual Machines

Containers have several advantages over traditional VMs:

- **Efficiency**: VMs require a fully installed operating system, while containers share the host OS, reducing resource consumption.

- **Speed**: Containers start quickly compared to VMs.

- **Resource Efficiency**: Containers consume fewer hardware resources compared to VMs.

## Docker Architecture

Docker is designed to work on various systems:

- On a Windows PC, Docker supports both Windows and Linux containers (Windows 10 even contains a Linux kernel).

- On a Linux system, Docker primarily runs Linux containers natively.

- On a Mac system, Docker uses a Linux VM to seamlessly run Linux containers.

## Docker Workflow

Here's a high-level overview of the Docker workflow:

### Step 1: Dockerize Your Application

An application is dockerized using the **Dockerfile**. The dockerfile is a plain text file that contains the instructions that docker uses to package this application into an **Image**.

### Step 2: Docker Images

This **Image** contains all the information that is needed by our application to run properly. Typically the **Image** contains the following things:

1. A cut down OS
2. A runtime environment
3. Application Files
4. Third-party libraries
5. Environment Variables

### Step 3: Containers

This **Image** is then used to start a **Container** by docker. A **Container** is a special type of process because it has its own type of file system which is provided by the **Image**.

### Step 4: Image Registry

Instead of running the file directly on the localhost/system, we tell docker to run the application inside a container in an isolated environment. Once we have an image we can push it to a registry like **Docker Hub**. This is just like Github for Git. It's a storage for Docker Images which can be used by anyone from anywhere. With Docker Hub you can **Build and Ship any Application Anywhere**.

### Step 5: Building and pushing a Docker Image on DockerHub

- Create a folder for your docker project. Eg. ```docker_project```
- Open folder in VSCode
- Create an app.js will the code : ```console.log("Hello Docker!);```
- Create a **Dockerfile** which contains all the information for the docker to run the application successfully containing the following code:
    ```FROM node:alpine```
    ```COPY . /app```
    ```WORKDIR /app```
    ```CMD node app.js```
- Create a docker image using the command : ```docker build -t docker_project .```
- Check the created docker images created on the system using the command: ```docker images``` or ```docker image ls```
- Login into dockerhub on the browser and create a repository that will contain the docker image which you have just created. For eg. name the repository as docker_project
- Login to the dockerhub in the CMD using command : ```docker login -u <YOUR USER NAME>``` and enter the docker password.
- Enter the command : ```docker tag getting-started YOUR-USER-NAME/docker_project```
- Push the docker image to the repository using command : ```docker push YOUR-USER-NAME/docker_project```
- To check the working of the docker image which is pushed to dockerhub, login to the website : <a href = "https://labs.play-with-docker.com/">play-with-docker</a>
- Create a new instance of the VM on play-with-docker.
- Pull the image from your repository on dockerhub : ```docker pull YOUR-USER-NAME/docker_project```
- Check whether the image is pulled successfully or not using, ```docker image ls```
- Run the image on the VM using, ```docker run YOUR-USER-NAME/docker_project```
- The output will be displayed on the terminal: **Hello Docker!**
