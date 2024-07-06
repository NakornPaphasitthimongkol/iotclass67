# Install Server and Docker

## How to install Server
1. download Ubuntu Server 24.04 to USB
2. Setup and apt-get update to Ubuntu Server
3. download tools such as vim, ifconfig, screen

    # install wireless-tools, net-tools, git, vim
    $ sudo apt install wireless-tools net-tools git vim

    # git clone project
    $ git clone https://github.com/sergio11/iot_event_streaming_architecture.git
4. set up Docker and Run
    # use vim edit file
    $ sudo vim /etc/docker/daemon.json

    # Put this text in the file.
    {
      "dns": ["8.8.8.8", "8.8.4.4"]
    }

    # restart service docker
    $ sudo systemctl restart docker

    # docker login
    $ sudo docker login

    # into project and docker compose
    $ cd iot_event_streaming_architecture
    $ sudo docker compose up
## How to install Docker

1. go to this website https://docs.docker.com/engine/install/ubuntu/
2. Set up Docker's apt repository.
   # Add Docker's official GPG key:
     sudo apt-get update
     sudo apt-get install ca-certificates curl
     sudo install -m 0755 -d /etc/apt/keyrings
     sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
     sudo chmod a+r /etc/apt/keyrings/docker.asc

   # Add the repository to Apt sources:
     echo \
        "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
        $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
        sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
     sudo apt-get update
3. Install the Docker packages.
  To install the latest version, run:
  sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
4. Verify that the Docker Engine installation is successful by running the hello-world image.
  sudo docker run hello-world
  This command downloads a test image and runs it in a container. When the container runs, it prints a confirmation message and exits.

You have now successfully installed and started Docker Engine.
