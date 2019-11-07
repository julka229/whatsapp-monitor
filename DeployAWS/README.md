# Deploy on AWS
## Architecture
### AWS
![architecture](/DeployAWS/architecture.jpg)


###### Let's Deploy this Script on AWS EC2 instances before deploy please setup in local first to save your Session Whatsapp data first run this script in local change your contact name in given script. To setup local follow same method (Skip 4th step) but atleast run local only one time for building profile (Save Whatsapp Session).

## 1. Install Chrome 
     sudo nano /etc/apt/sources.list.d/google-chrome.list
     paste deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main
     sudo apt-key add linux_signing_key.pub
     sudo apt update
     sudo apt install google-chrome-stable
     google-chrome --version


## 2. Install ChromeDriver
    wget https://chromedriver.storage.googleapis.com/78.0.3904.70/chromedriver_linux64.zip
    unzip chromedriver_linux64.zip 
    sudo mv chromedriver /usr/bin/

## 3. Install Requirements
      pip3 install selenium notify_run --user

## 4. Upload Your Session and Script to Instance
      scp -i {pem file path} {your file path} {ubuntu@your_instance_address}:/home/ubuntu/

## 5. Register Push Notification

     notify-run register and subscribe from url 
     
## 6. Run Script aws.py
       