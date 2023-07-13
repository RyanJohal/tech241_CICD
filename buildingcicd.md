# Building Jenkins Env
1. Launch ec2, ubuntu 18.04
2. Security group inbound ports: ssh, http, https, 8080
3. First, update the default Ubuntu packages lists for upgrades with the following command:
```sudo apt-get update```
4. Then install Java8 or above (I done 11)
```sudo apt-get install openjdk-11-jdk```
5. Now install jenkins itself:
```
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins 
```
6. For jenkins to start it needs to be enabled
```sudo systemctl enable jenkins```
7. Start jenkins
```sudo systemctl start jenkins```
8. Check status if jenkins is running and to access key pass
```sudo systemctl status jenkins```
9. Once logged into jenkins you need to install nodejs plugin and ssh build agents plugin, in addition to the default plugins jenkins has set.
10. Change node js version to 12 by going manaage jenkins - tools - node js version - 12.x
11. Add webhook to github payload:http://localip:8080/github-webhook/, content type: application/json, trigger with push and pull.
 
![Alt text](<images/MicrosoftTeams-image (4).png>)


![Alt text](images/gitworkflow.jpg)

