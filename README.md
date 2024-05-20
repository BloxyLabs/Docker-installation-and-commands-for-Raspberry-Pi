# Docker-installation-and-commands-for-Raspberry-Pi
Here you can find everything about Docker and Docker Compose installation on a Raspberry Pi and commands you can use
<br>
<br>
Check also our YouTube channel for instructions and other related information [YouTube](https://www.youtube.com/@bloxylabs "YouTube").
<br>
If you had fun with the projects, please consider buying us a [cup of coffee](https://www.buymeacoffee.com/bloxylabs "cupofcoffee") :coffee:.

<h3><u>The commands to update and upgrade your Pi</u></h3>

```
sudo apt update
```
```
sudo apt upgrade
```
<h3><u>The command to install Docker to your Pi</u></h3>

```
curl -sSL https://get.docker.com | sh

```

<h3><u>Adding non-root user to the Docker group</u></h3>
To avoid having to type sudo for every command, you can add the non-root user to the Docker group. Replace $USER with the user name. For example "Pi" if that is your default user.

```
sudo usermod -aG docker $USER
exit
Login again to your Pi
```
<h3><u>The commands to install Docker Compose to your Pi</u></h3>

```
sudo apt install docker-compose

```
<h3><u>Checking installed versions of Docker and Docker Compose</u></h3>

```
docker -v

docker-compose -v

```





# Basic Docker commands

List Docker volumes:
```
docker volume ls
```
Create a new volume type:
```
docker volume create myvol
```
Remove a volume:
```
docker volume rm myvol
```
Mount a volume:
```
docker run --mount source=myvol,target=/app
```
Where myvol=name of the volumen and /app=mount point/path within the container.
<br>
<br>
Pull an image from a registry:
```
docker pull docker/getting-started
```
To get an image list:
```
docker image ls
```
Remove unused images:
```
docker image prune
```
Run a container interactively over tty:
```
docker run -it
```
Remove a specific image:
```
docker images rm imagename
```
List all the containers including those not in use:
```
docker container ls -all
```
Connect a running container:
```
docker attach
```
Stop a running container from within a container:
To disconnect from a running container type ctrl-p, ctrl-q
```
exit
```
List all running containers:
```
docker ps
```
-p is for mapping ports from the host to the container
```
docker run -p 80:80
```
