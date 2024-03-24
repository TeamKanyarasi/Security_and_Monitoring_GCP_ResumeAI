# ResumeAI

## Overview
The project is a MEAN project and uses node version 18.

## A web application where you can build your resumes
- Specify your job description, get a resume generated.
- Edit it according to your will using the editor provided by the website.

## Features

- Resume Auto Generation based on job description using OpenAI.
- An editor to edit your resume according to your needs, some features included:

    - Change colors of headers,sections and text.
    - Inline editing making typing easier
    - 3 different alignments for the body of resume
    - Drag functionality to move sections up and down
    - Can add an image, image can be cropped with the cropper provided.
    - Zooming functionality 
- Send resume to your email.
- Various subscription levels.

## Running The Project

![Screenshot (195)](https://github.com/TeamKanyarasi/Security_and_Monitoring_GCP_ResumeAI/assets/139607786/555b139f-61d4-4d79-9905-a61c3b590868)

### Running The Backend 
- Git clone the respository
```bash
  git clone https://github.com/TeamKanyarasi/Security_and_Monitoring_GCP_ResumeAI.git
```
- Move into the directory
```bash
  cd  backend
```
- Install npm dependencies 
```bash
npm i --force
```
- Create a .env file with following fields
```bash
JWT_SECRET_KEY="MYREALLYSECRETKEY"
MONGO_URL="mongodb://MONGO_URL"
OPENAI_KEY="OPENAI_API_KEY"
GMAIL_USER="THIS EMAIL IS USED TO SEND RESUMES"
GMAIL_PASS="PASSWORD USED BY NODEMAILER"
FRONT_END="URL FOR FRONTEND"
```
- Now run the code
```bash
  nohup node src/main/index.js & 
  
  or

  nohup npm start &

  or

  npm start
```

![Screenshot (196)](https://github.com/TeamKanyarasi/Security_and_Monitoring_GCP_ResumeAI/assets/139607786/e91012aa-78ff-4df8-b296-385a58ce8749)

![Screenshot (194)](https://github.com/TeamKanyarasi/Security_and_Monitoring_GCP_ResumeAI/assets/139607786/5dd67ea8-1451-47d6-bf27-16037e587bbd)

### Running The Frontend
- Git clone the respository
```bash
  git clone https://github.com/TeamKanyarasi/Security_and_Monitoring_GCP_ResumeAI.git
```
- Move into the directory
```bash
  cd  frontend
```
- Install npm dependencies 
```bash
npm i --force
```

- Make sure angular-cli is installed
```bash
npm install -g @angular/cli
```
- Run the application [ In development mode]
```bash
  #This runs the application in development mode 
  #And the backend must be running on port 4292
  #If the port of backend is changed then
  #Edit it in the proxy.conf.json
  
  npm start
  ```

![Screenshot (197)](https://github.com/TeamKanyarasi/Security_and_Monitoring_GCP_ResumeAI/assets/139607786/2dbf360b-9bb7-4307-8067-b77ca48af2b9)

#### You have now succesfully deployed the application

## Security and Monitoring
 - Enable monitoring on VM instances.
 - Create a Custom Dashboard with required metrics.

![Screenshot (198)](https://github.com/TeamKanyarasi/Security_and_Monitoring_GCP_ResumeAI/assets/139607786/9c2dbb0e-7d56-4578-a1ec-5af1ccea1263)
