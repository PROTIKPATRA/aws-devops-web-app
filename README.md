# 🚀 AWS DevOps Web App – CI/CD Pipeline Project

## 📌 Project Overview

This project demonstrates a complete **CI/CD (Continuous Integration & Continuous Deployment)** pipeline using AWS services.
The application is a simple web app (HTML, CSS, JavaScript) automatically built and deployed to an EC2 instance whenever code changes are pushed.

---

## 🏗️ Architecture

The pipeline integrates the following AWS services:

* AWS CodeCommit – Source code repository
* AWS CodeBuild – Build and artifact generation
* AWS CodeDeploy – Deployment to EC2
* AWS CodePipeline – CI/CD orchestration
* Amazon S3 – Artifact storage
* Amazon EC2 – Hosting the web application

---

## 🔄 CI/CD Workflow

1. Developer pushes code to CodeCommit
2. CodePipeline detects changes automatically
3. CodeBuild runs `buildspec.yml` to prepare artifacts
4. Artifacts are stored in S3 bucket
5. CodeDeploy deploys application to EC2 instance
6. Web app is updated automatically

---

## 📂 Project Structure

```
Aws-wep-app/
│── index.html
│── style.css
│── script.js
│── buildspec.yml
│── appspec.yml
│
└── scripts/
    ├── install_nginx.sh
    └── start_nginx.sh
```

---

## ⚙️ Build Configuration (buildspec.yml)

* Prepares application files
* Packages artifacts for deployment
* Sends output to S3

---

## 🚀 Deployment Configuration (appspec.yml)

* Defines file copy location (`/var/www/html`)
* Executes scripts for installing and starting NGINX

---

## 🖥️ EC2 Setup

* Ubuntu / Amazon Linux instance
* CodeDeploy Agent installed
* IAM Role attached with:

  * S3 access
  * CodeDeploy permissions

---

## 🌐 Features of the Web App

* Interactive UI with button actions
* Live system time display
* Visitor counter (local storage)
* Deployment version information
* Clean and responsive design

---

## 📦 S3 Artifact Storage

Build artifacts are stored in:

```
s3://aws-web-app-bucket/code_output/
```

These artifacts are used by CodeDeploy for deployment.

---

## 🔐 IAM Roles Used

### EC2 Role:

* AmazonS3ReadOnlyAccess
* AmazonEC2RoleforAWSCodeDeploy

### CodeBuild Role:

* S3 access
* Logs permissions

### CodeDeploy Role:

* AWSCodeDeployFullAccess

---

## 📊 Pipeline Stages

```
Source (CodeCommit)
   ↓
Build (CodeBuild)
   ↓
Deploy (CodeDeploy)
```

---

## 🧠 Key Learnings

* End-to-end CI/CD pipeline implementation
* Debugging real-world deployment issues
* Working with IAM roles and permissions
* Handling build artifacts and S3 integration
* Automating deployments to EC2

---

## 🚧 Challenges Faced

* CodeDeploy agent installation issues (Ubuntu vs Amazon Linux)
* IAM permission errors
* S3 artifact path misconfiguration
* GitHub authentication issues (PAT vs password)

---

## 🏆 Outcome

Successfully built a fully automated CI/CD pipeline where:

✔ Code changes trigger automatic deployment
✔ No manual intervention required
✔ Application is continuously updated on EC2

---

## 🔮 Future Enhancements

* Add automated testing stage
* Implement Docker + ECS deployment
* Add monitoring with CloudWatch
* Enable Blue-Green deployment strategy

---

## 📸 Screenshots

<img width="2880" height="1710" alt="image" src="https://github.com/user-attachments/assets/286627bf-7f37-49ea-ac72-ecbad09cbdfe" />
<img width="2876" height="1720" alt="image" src="https://github.com/user-attachments/assets/ffc16393-fd67-416a-a290-267c15354283" />
<img width="2876" height="1708" alt="image" src="https://github.com/user-attachments/assets/d6b56293-907f-4322-9c74-be5ee9653fe9" />
<img width="2880" height="1714" alt="image" src="https://github.com/user-attachments/assets/eddee146-e4e1-46ed-9496-ef4fc87d1c08" />
<img width="2874" height="1702" alt="image" src="https://github.com/user-attachments/assets/1a698dbf-62c2-4b7f-8e32-e0f11602df30" />
<img width="2880" height="1726" alt="image" src="https://github.com/user-attachments/assets/de336e0c-e6e3-4f22-b510-bc0760e327df" />
<img width="2880" height="1726" alt="image" src="https://github.com/user-attachments/assets/27b57492-1db5-49ca-aea2-2bd3a63411c0" />
<img width="2880" height="1726" alt="image" src="https://github.com/user-attachments/assets/9dfee40f-1452-4a93-8efb-544fa19bd898" />



---

## 👨‍💻 Author

**Protik Patra**  
DevOps Engineer

---

## ⭐ Conclusion

This project demonstrates practical implementation of DevOps concepts using AWS, showcasing automation, scalability, and real-world deployment workflows.
