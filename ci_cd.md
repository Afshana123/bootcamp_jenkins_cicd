# CI/CD Pipeline 
Continuous Integration and Continuous Delivery Pipeline 

#### SDLC 
Software development life cycle based on:
-plan/design
-develop
-test
-deploy

#### Problems in traditional SD;C
- Scale and complexity	
	- Function
	- Architecture 
	- Infrastructure
	- Developer
	- Operations
- Manual and slow processes
- Broken communication
- Human errors
-

#### DevOps in SDLC
- DevOps come to help modern SDLC - Agile
	- Collaboration 
	- Automation
- DevOps Lifecyle 
<insert image>

#### DevOps Lifecycle Stages 
- Continuous Development 
- Continuous Testing 
- Continuous Integration
- Continuous Delivery/Deployment 
- Continuous Monitoring 

#### CI - Continuous Integration
Continous Integration(CD) is the practice of merging all developers workng copies to a shared mainline several times a day.
- Development
- Testing
- Integration 

Continuous deployment - goes live in front of the users so if something goes wrong then it will appear wrong live

#### Why CI/CD Matters?
- reduce costs
- faster release rate
- smaller code changes
- fault isolations 
- more test reliability 
- increase team transparency and accountability 
- easy maintenance and updates 

#### Conclusion

DevOps helps
- culture
- people.teams 
- collaboration
- principles 

#### Jenkins 
Multi Billion Dollar companies like Facebook, Netflix and Ebay have adopted Jenkins because of it’s amazing advantages, Jenkins is an open-source automation server in which the central build and CI process take place, It is a Java-based program with packages for Windows, macOS, & Linux.

Tools available similar to Jenkins:
- circleci
- TeamCity
- Bamboo 
- GitLab 


cd ~/.ssh
ssh-keygen -t rsa -b 4096 -C "your_email@githubemail.com"

Create a webhook on github that listens to any changes/pushes from you localhost and triggers your job in jenkins 

https://www.blazemeter.com/blog/how-to-integrate-your-github-repository-to-your-jenkins-project

make changes in your github and refresh your Jenkins page - you should see a new build

Provided that tests have passed, the next job should trigger to merge code into master/main brach 
- Create a branch called dev 
- Create a newjob on Jenkins called afshana-ci-merge to merge dev into main if the first job was successful 
- testing123456

