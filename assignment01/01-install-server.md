# Install Server and Docker

## How to install Server
1.download Ubuntu Server to USB\n
2.Setup and apt-get update to Ubuntu Server\n
3.download tools such as vim, ifconfig, screen\n

## How to install Docker

1.go to this website https://docs.docker.com/engine/install/ubuntu/\n
2.Set up Docker's apt repository.\n
Add Docker's official GPG key:\n
sudo apt-get update\n
sudo apt-get install ca-certificates curl\n
sudo install -m 0755 -d /etc/apt/keyrings\n
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc\n
sudo chmod a+r /etc/apt/keyrings/docker.asc\n

Add the repository to Apt sources:\n
echo \\n
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \\n
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \\n
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null\n
sudo apt-get update\n
3.Install the Docker packages.\n
To install the latest version, run:\n
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin\n
4.Verify that the Docker Engine installation is successful by running the hello-world image.\n
sudo docker run hello-world\n
This command downloads a test image and runs it in a container. When the container runs, it prints a confirmation message and exits.\n

You have now successfully installed and started Docker Engine.\n
