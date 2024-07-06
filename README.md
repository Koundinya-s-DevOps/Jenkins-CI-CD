# Jenkins-CI-CD
#### Step 1: Initialized the GitHub Repo
#### Step 2: Create and EC2 Instance in AWS or Virtual Machine in MS Azure
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


