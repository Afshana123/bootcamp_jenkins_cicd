# Let's build a Continuous Integration and Continuous Delivery/Deployment (CICD) Pipeline
## Jenkins
### Webhooks with Git-hub
#### Automated Testing using Jenkins
#### Automated Deployment on AWS EC2 for 2Tier architecture - Nodejs app and Mongodb  


- Jenkins Workflow
  
![](images/jenkins.png)

  ##### Contiounus Integration Continuous Delivery/Deployment 
![](images/CICD.png)

- We have a private SSH key available  - create a secure connection between local host and github 
- Source code is also available on Git
- webhook will listen in on Github when it recieves something to jenkins
- Configure webbook in Github 
- Generate another SSH Key - to have a secure connection between Github and Jenkins
- Building a secure pipeline 
- Give a private key to Jenkins 
- Jenkins can clone the repo in a secure environment with ssh authentication
- Do testing in Agent Node because Jenkin server will still run and facilitate users even if it breaks 
- Agent Node Server 

###### Let's break it down 
  ![](images/cicd_jenkins.png)

Task list: 
- Github repo with source code
- SSH set up
- App code available on github
- cd app
- npm install
- npm test -automated 
- testing 
- npm start

Problems/debugging:
- SSH key not set up correctly



### For deployment job in Jenkins
- In the execute shell of CD job

```
# we need to by pass the key asking stage with below command:
ssh -A -o "StrictHostKeyChecking=no" ubuntu@ec2-ip << EOF	
# copy the the code
# run your provision.sh to install node with required dependencies for app instance - same goes for db instance (ensure to double check if node and db are actively running)

# create an env to connect to db
# navigate to app folder
# kill any existing pm2 process just in case
# launch the app
nohup node app.js > /dev/null 2>&1 & - use this command to run node app in the background

# To debug ssh into your ec2 and run the above commands
    

EOF
```
## Jenkins CI Lab - Solution

##### Steps

##### Source Code Management

1. Set Branches to Build to develop
2. Under additional behaviours click add and "Merge before build"
3. name of repo "origin"
4. branch to merge "main"

### Post-Build Actions

#### Git Publisher

1. Add Post Build Action
2. Git Publisher
3. Push Only if Build Succeeds
4. Merge Results

--- 
Tigger deployment job if the merge was successfull
