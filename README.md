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

# Basic Ollama commands

Check if OLLAMA is running:
```
sudo systemctl status ollama
```
List all installed Large Language Models:
```
ollama list
```
List of possible commands:
```
ollama --help
```
Run an installed model:
```
ollama run <installed model name>
```

