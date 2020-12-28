# Install Teslamate on raspberry pi

We start from the point that your Raspbian is already installed, ssh is enabled and has a fixed ip adress configured

The following steps are needed to install Docker en Docker Compose on a raspbian Linux.

### Download the docker installer script

`curl -fsSL https://get.docker.com -o get-docker.sh`

### Execute the docker install script

`sudo sh get-docker.sh`

### Add permission to Pi User to run Docker Commands

`sudo usermod -aG docker pi`

### IMPORTANT! Install proper dependencies

`sudo apt-get install -y libffi-dev libssl-dev`
`sudo apt-get install -y python3 python3-pip`
`sudo apt-get remove python-configparser`

### Install Docker Compose

`sudo pip3 -v install docker-compose`

Reboot here or run the next commands so you can run the docker compose command without sudo

In the folders Management en Teslamate you will find the needed YML files to run your docker compose.

More details installation instruction can be found on https://docs.teslamate.org/
