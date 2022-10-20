## Install Docker CE on Ubuntu 20.04
 
`sudo apt update`

`sudo apt install apt-transport-https ca-certificates curl software-properties-common`

`curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`

`sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"`

`apt-cache policy docker-ce`

`sudo apt install docker-ce`

`sudo systemctl status docker`

## Add current user to Docker Group
 
`sudo usermod -aG docker ${USER}`

`su - ${USER}`

`groups`

`docker version`

## Install Docker Compose (Optional)
 
`sudo apt-get update`

`sudo apt-get install docker-compose-plugin`

`docker compose version`

## Plan I: Use Image
