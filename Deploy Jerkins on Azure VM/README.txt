Deploy Jenkins on Azure VM (Ubuntu)

This project demonstrates how to deploy Jenkins on an Ubuntu Virtual Machine hosted on Microsoft Azure.
It covers the end-to-end setup — from creating the VM to accessing Jenkins via a web browser.

 Steps Overview
1. Create Azure Resources

Created a Resource Group in Azure.

Created an Ubuntu Virtual Machine with SSH authentication.

During setup, downloaded the SSH key pair for secure access.

2. Connect to the VM

Installed Git Bash on the local computer.

Connected to the Ubuntu VM using its public IP address via SSH:

ssh -i <private-key.pem> azureuser@<VM-Public-IP>


Confirmed the Ubuntu VM is up and running.

3. Install Prerequisites (Java)

Before installing Jenkins, installed Java (required to run Jenkins):

sudo apt update
sudo apt install openjdk-11-jre -y
java -version

4. Install Jenkins

Added the Jenkins repository key and package source:

wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'


Installed Jenkins:

sudo apt update
sudo apt install jenkins -y


Started and enabled the Jenkins service:

sudo systemctl start jenkins
sudo systemctl enable jenkins


Verified Jenkins is running:

ps -ef | grep jenkins

5. Configure Azure Networking

Created an inbound security rule in the Network Security Group (NSG) to allow TCP port 8080 (required for Jenkins access).

6. Access Jenkins

Opened Jenkins in a web browser:

http://<VM-Public-IP>:8080


Example:
http://40.82.192.255:8080

Unlocked Jenkins using the initial admin password:

sudo cat /var/lib/jenkins/secrets/initialAdminPassword


Completed the setup wizard and installed suggested plugins.

 Verification

Once setup is complete:

Jenkins dashboard is accessible.

Service is active and enabled on system boot.

Jenkins is ready for pipeline creation and job automation.

 Notes

Replace <private-key.pem> and <VM-Public-IP> with your actual file and IP.

Ensure port 8080 is open in your Azure Network Security Group.

You can stop/start the service anytime using:

sudo systemctl stop jenkins
sudo systemctl start Jenkins

Jenkins successfully deployed and accessible via:
http://<VM-Public-IP>:8080