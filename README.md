##Docker

Refer: https://docs.docker.com/get-started/docker-overview/

👉Docker is an open-source platform that enables developers to build, ship and run applications in containers.
Docker enables to separate our applications from our infrastructure so we can deliver software quickly.

What is a container?

👉Container is a lightweight, standalone and executable software packages; the packages include,
Application code -- Libraries and dependencies -- Runtime -- Configuration files

##Insatll Docker on Linux server:

Refer: https://docs.docker.com/engine/install/ubuntu/

```
# Add Docker's official GPG key:
sudo apt update
sudo apt install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
sudo tee /etc/apt/sources.list.d/docker.sources <<EOF
Types: deb
URIs: https://download.docker.com/linux/ubuntu
Suites: $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}")
Components: stable
Signed-By: /etc/apt/keyrings/docker.asc
EOF

sudo apt update
```
To install the latest version, run:
```
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
The Docker service starts automatically after installation. To verify that Docker is running, use:
```
sudo systemctl status docker

#Some systems may have this behavior disabled and will require a manual start:

sudo systemctl start docker
```

🔗There are lots of pre-built docker images, refer: https://hub.docker.com/

