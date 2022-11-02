# Docker-IDE
This is a repo for a FDG Project: *Implementation of Cloud & Dockerization Technology in Computer Science Education*.

The goal is to deploy an IDE web app on local/remote server/VM using docker containers. Students in programming class can also access the IDE during the class and Q & A session.

[]()

## Plans
### Web IDE
- Based on [Code Server](https://github.com/coder/code-server).
- Support dependencies for different programming languages
- Build from docker image
- Support VS Code extensions

### Platform Coder
- Based on [Coder](https://github.com/coder/coder).


## Images
| Image | Tag | Description |
| ------ | ----- | ----------- |
| tisage/ide | test	| Testing |

| image | Tag | Description |
| ------ | ----- | ----------- |
| tisage/coder | test	| Still testing |

## Requirements
- Install Docker client (See [setup.md](https://github.com/tisage/Docker-IDE/blob/main/Setup.md) file)
- A Web Port Open

## Installation
- Pull Docker Images & Run the container using command line

### Create a folder `ide` to mount
`mkdir ide`

Change the `YOUR_PASSWORD` which will be used to login the web app.
### Linux/Mac OS
`docker run -d --name=code-server -p 80:8080 -e PASSWORD=YOUR_PASSWORD -v $(pwd)/:/home/coder --restart unless-stopped tisage/ide:test`

### Windows OS Command Line
`docker run -d --name=code-server -p 80:8080 -e PASSWORD=YOUR_PASSWORD -v %cd%/ide/:/home/coder --restart unless-stopped tisage/ide:test`

### Windows OS PowerShell
`docker run -d --name=code-server -p 80:8080 -e PASSWORD=YOUR_PASSWORD -v ${PWD}/ide/:/home/coder --restart unless-stopped tisage/ide:test`

Open host IP's port `80` 
(default use `80`, can customize other port number)

**Extension bug**: need to install extension manually after running the container instance


2022

v 0.8
