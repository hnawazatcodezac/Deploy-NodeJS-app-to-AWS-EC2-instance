# Deploy-NodeJS-app-to-AWS-EC2-instance

## 1. Create the AWS EC2 Instance

- Create an AWS account, if you don’t have one then navigate to the EC2 instances page and click the Launch Instances button.
- Create the new key pair. Give any name to key pair for example node-app. Download the keypair and save it in your machine.
- Last step is to launch the instance. 

---

## 2. SSH Into Your Instance & Install Prerequisites

- SSH into instance by running the command:
  `ssh -i keypair_name.pem ubuntu@ip-address`
  
- Update the packages by running the command:
  `sudo apt-get update`

- Install NodeJS by running the command:
  `sudo apt-get install -y nodejs`

- Install Git by running the command:
  `sudo apt-get install git`
  
- Clone the github repo:
  `git clone [repo-link]`

- Navigate to directory:
  For example: cd node-app or cd test
  
- Install dependencies:
  `npm install`

- Run the app:
  `npm start index.js`
  
- App is running now. Install pm2 for running the app forever in the background by running the command:
  `sudo npm install pm2 -g`

- Run the app:
  `sudo pm2 start index.js`
  
- Stop the app:
  `sudo pm2 stop index.js`
