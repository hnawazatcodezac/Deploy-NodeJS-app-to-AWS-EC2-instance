# Deploy Node.js App to AWS EC2 Instance

## 📺 YouTube Tutorial  
[Watch Tutorial](https://www.youtube.com/watch?v=8savIXlU3wA&t=17s)

---

## 1. Create the AWS EC2 Instance

- Create an AWS account if you don’t have one.
- Navigate to the **EC2 Instances** page and click the **Launch Instances** button.
- Create a new key pair.  
  Give it a name (e.g., `node-app`) and download the `.pem` key file — save it safely on your machine.
- Proceed through the remaining steps to launch the instance.

---

## 2. SSH Into Your Instance & Install Prerequisites

- SSH into instance by running the command:
  `ssh -i keypair_name.pem ubuntu@ip-address`
  
- Update the packages by running the command:
  ```bash
    sudo apt-get update
  ```

- Install NodeJS by running the command:
  ```bash
    sudo apt-get install -y nodejs
  ```

- Install Git by running the command:
  ```bash
    sudo apt-get install git
  ```

- Clone the github repo:
  ```bash
    git clone [repo-link]
  ```

- Navigate to directory:
  For example:
    ```bash
      cd node-app or cd test
    ```
  
- Install dependencies:
  ```bash
    npm install
  ```

- Run the app:
  ```bash
    npm start index.js
  ```
  
- App is running now. Install pm2 for running the app forever in the background by running the command:
  ```bash
    sudo npm install pm2 -g
  ```

- Run the app:
  ```bash
    sudo pm2 start index.js
  ```
  
- Stop the app:
  ```bash
    sudo pm2 stop index.js
  ```
