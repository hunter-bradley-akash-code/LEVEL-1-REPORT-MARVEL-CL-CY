# TASK 1: Working with Git and GitHub

---

In this task, I learned the basics of **Git and GitHub** and how they are used for version control, managing different versions of a project, and collaborating with other developers.

I started by creating a simple Python calculator and used Git to track the changes made to it. I created branches for adding new operations, merged the changes into the main branch, and explored different ways of managing commits using `git revert` and `git cherry-pick`.

## Git Basics

I practiced the basic Git workflow by creating a local repository and tracking changes made to the calculator program.

Some of the commands I used were:

| Command | Purpose |
|---|---|
| `git init` | Creates a new Git repository |
| `git status` | Shows the current status of the repository |
| `git add` | Moves changes to the staging area |
| `git commit` | Records changes in Git history |
| `git log` | Displays the commit history |
| `git branch` | Creates or lists branches |
| `git checkout` | Switches between branches |
| `git merge` | Combines changes from one branch into another |
| `git remote` | Manages connections to remote repositories |
| `git push` | Uploads local commits to GitHub |
| `git clone` | Downloads a repository from GitHub |

I created separate branches for the calculator features and worked on them independently before merging them into the `master` branch.

## Git Revert

I used `git revert` to undo the **power operation** that had been added to the calculator.

Instead of deleting the original commit, Git created a new commit that reversed the changes made by that commit. This helped me understand how Git maintains the complete history of a project even when changes need to be undone.

## Git Cherry-Pick

After reverting the power operation, I used `git cherry-pick` to apply the original power-operation commit back to the current branch.

```bash
git cherry-pick <commit id>
```

## Open-Source Contribution

As part of this task, I also learned how to contribute to an open-source project using GitHub.

I forked the **TheAlgorithms/Python** repository to my GitHub account and cloned the fork to my local system. I then created a separate branch called `add-simple-algorithm` so that my changes could be developed independently from the main branch.

I added a new **Harmonic Mean** algorithm in the existing `maths` directory.

## IMAGES
---

# TASK 2: Exploring Docker Fundamentals

---

In this task I learned the fundamentals of **Docker** and how containers are used to run applications in an isolated and lightweight environment. I started by understanding the difference between **containers and virtual machines**, and then practiced basic Docker commands using the Docker CLI.

A **Docker image** acts as a template containing the files, dependencies and configuration required to run an application, while a **container** is a running instance of that image. I also explored **Docker Hub**, which is a public registry where Docker images can be stored and shared.

## Understanding Containers and Virtual Machines

A **virtual machine** runs a complete guest operating system on top of a hypervisor. Since each virtual machine includes its own operating system, it generally requires more storage and system resources.

A **container**, on the other hand, shares the host operating system kernel while isolating the application and its dependencies. This makes containers lightweight, faster to start and convenient for deploying applications.

| Feature | Containers | Virtual Machines |
|---|---|---|
| Virtualization | Operating-system level | Hardware level |
| Operating System | Shares the host kernel | Has its own guest OS |
| Startup | Usually very fast | Usually slower |
| Resource Usage | Lower | Higher |
| Size | Generally smaller | Generally larger |
| Isolation | Application/process level | Machine level |

This comparison helped me understand why Docker containers are widely used for application development, testing and deployment.

## Docker Containers and Commands

I used Docker CLI commands to pull the **Ubuntu** image from Docker Hub and run it as a container. I also worked with an **Nginx** container by mapping its port and accessing the Nginx welcome page through the browser.

I practiced commands to view running containers, check container logs, inspect container details and view running processes. Finally, I managed the container lifecycle by starting, stopping, restarting and removing containers.

This task gave me a practical understanding of how Docker images and containers work and how containers can be managed using the command line.

## Important Docker Commands

| Command | Purpose |
|---|---|
| `docker --version` | Checks the installed Docker version |
| `docker pull <image>` | Downloads an image from Docker Hub |
| `docker images` | Lists downloaded Docker images |
| `docker run <image>` | Creates and runs a container |
| `docker ps` | Shows running containers |
| `docker ps -a` | Shows all containers |
| `docker start <container>` | Starts a stopped container |
| `docker stop <container>` | Stops a running container |
| `docker restart <container>` | Restarts a container |
| `docker logs <container>` | Displays container logs |
| `docker inspect <container>` | Shows detailed container information |
| `docker top <container>` | Shows processes running in a container |
| `docker exec -it <container> <command>` | Executes a command inside a running container |
| `docker rm <container>` | Removes a container |
| `docker rmi <image>` | Removes a Docker image |

## Images

- - -

# TASK 3: Dockerize a Simple Application
---

In this task I learned how to containerize a simple static website using Docker. I created a multi-page website using **HTML, CSS and JavaScript** and used **Nginx** to serve the website inside a Docker container.

I created a `Dockerfile` using instructions such as `FROM`, `LABEL`, `WORKDIR`, `COPY`, `EXPOSE` and `CMD`. I also created a `.dockerignore` file to avoid including unnecessary files in the Docker build context.

After creating the files, I built a Docker image and ran it as a container with port mapping. I accessed the website through the browser and tested its different pages and JavaScript functionality.

I also practiced useful Docker commands such as `docker logs`, `docker inspect` and `docker exec` to check and explore the running container. Finally, I stopped, started, restarted and removed the container to understand the basic Docker container lifecycle.

I created a `Dockerfile` to define how the website should be built and run inside the Docker container. The main instructions used in the Dockerfile were:

| Dockerfile Instruction | Purpose |
|---|---|
| `FROM nginx:latest` | Uses the latest Nginx image as the base image. |
| `LABEL maintainer="Akash"` | Adds information about the maintainer of the image. |
| `LABEL description="Docker Task 3 - Static Website"` | Describes the purpose of the Docker image. |
| `WORKDIR /usr/share/nginx/html` | Sets the working directory where the website files are stored. |
| `COPY website/ .` | Copies the website files from the local `website` folder into the Nginx web directory. |
| `EXPOSE 80` | Indicates that the container uses port 80 for the web server. |
| `CMD ["nginx", "-g", "daemon off;"]` | Starts Nginx in the foreground when the container runs. |

This task helped me understand how a Dockerfile is used to create an image and how an application can be packaged and run consistently inside a container.


## Images

- - -

# TASK 4: Launch and Manage an AWS EC2 Instance
---

In this task I explored **AWS EC2** and learned how to launch and manage a virtual machine in the cloud. I created a **t3.micro EC2 instance** using Amazon Linux 2023 and configured the security group to allow SSH and HTTP traffic.

I created and used a **.pem key pair** to securely connect to the instance through SSH. After connecting, I installed and configured **Nginx** as a lightweight web server and confirmed that it was running and accessible through the instance's public IP address.

I also checked the CPU and memory resources available to the virtual machine using `lscpu` and `free -h`. The instance provided **2 vCPUs** and around **913 MiB of memory**. I also understood that the `t3.micro` is a burstable instance type that uses **CPU credits** when additional CPU performance is required.

Overall, this task gave me practical experience with launching an EC2 instance, securely accessing it, configuring network access, hosting a web server, and understanding the basic CPU and memory resources of a cloud VM.

## Images

- - -
