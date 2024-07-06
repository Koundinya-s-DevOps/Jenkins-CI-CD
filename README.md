# Jenkins-CI-CD
### Step 1: Initialized the GitHub Repo
### Step 2: Create and EC2 Instance in AWS or Virtual Machine in MS Azure
######  Install the Java in the EC2 Instance, As Jenkins is a Java Based Program.
        sudo apt update
        sudo apt install openjdk-11-jre
###### Verify the Java Installation
        java --version
###### Install the Jenkins by Below Commands
        sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
          https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
        echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
          https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
          /etc/apt/sources.list.d/jenkins.list > /dev/null
        sudo apt-get update
        sudo apt-get install jenkins
###### Check Jenkins Installation
        ps -ef | grep jenkins
###### Open the Jenkins in the new Browser Tab http://[PUBLIC_IPADDRESS]:8080(If the port is 8080)
###### Complete the Jenkins Setup and create a user account (or) keep admin as default user account
###### Create on Standard Plugin configuration and wait for the Jenkins to complete and restart.
### Step 3: Docker Slave Configuration
###### Install docker
        sudo apt update
        sudo apt install docker.io
###### Grant Jenkins user and Ubuntu user permission to docker deamon.
        sudo su -
        usermod -aG docker jenkins
        usermod -aG docker ubuntu
        systemctl restart docker
###### Restart Jenkins
        http://[PUBLIC_IPADDRESS]:8080/restart
