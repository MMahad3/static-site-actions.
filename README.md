# 🚀 Static Website with CI/CD using GitHub Actions & AWS

This project demonstrates how to **deploy a static website** on **AWS S3 + CloudFront** with a **fully automated CI/CD pipeline** powered by **GitHub Actions**.  

Whenever changes are pushed to the repository, GitHub Actions automatically:  
1. Builds and syncs the website to a private **S3 bucket**.  
2. Invalidates the **CloudFront cache** so the latest version is served globally. (not implemented yet) 

---

## ✨ Features
- 🌐 Static website hosted on **AWS S3** (private bucket).  
- ⚡ Global content delivery via **AWS CloudFront**.  
- 🔐 Secure deployment with **GitHub Secrets**.  
- 🔄 Fully automated **CI/CD pipeline** using GitHub Actions.  
- 🛠️ Branching workflow with `main` as the production branch.  

---

## ⚙️ CI/CD Workflow
The pipeline is defined in `.github/workflows/ci.yml`.  
It performs the following steps:  

1. **Checkout Code** – Pulls the repo code into the workflow runner.  
2. **Sync to S3** – Uploads updated files to the S3 bucket.  
3. **CloudFront Invalidation** – Clears old cached content so new changes appear instantly.  

---

## 🔑 Secrets Configuration
The following secrets must be stored in your **GitHub Repository → Settings → Secrets and variables**:  

- `AWS_ACCESS_KEY_ID` – IAM user access key.  
- `AWS_SECRET_ACCESS_KEY` – IAM user secret.  
- `AWS_REGION` – Region where S3 bucket & CloudFront are configured (e.g., `us-east-1`).  
- `S3_BUCKET` – Name of your S3 bucket.  
- `CLOUDFRONT_DISTRIBUTION_ID` – Distribution ID for CloudFront.  

---

## 🚀 Deployment
- Push code to the `main` branch → GitHub Actions automatically deploys it.  
- No manual S3 upload or CloudFront invalidation needed.  

---

## 📖 Learning Outcomes
From this project, I learned:  
- ✅ How to work with **Git branching**.  
- ✅ How to write **YAML workflows** for GitHub Actions.  
- ✅ How to set up **CI/CD pipelines**.  
- ✅ How to use **GitHub Secret Manager** securely.  
- ✅ How to deploy a **static website on AWS with full CI/CD automation**.  

---

## 📌 Next Steps
- Add **linting & testing** in the pipeline for future projects.  
- Extend this pipeline for a **MERN or Dockerized app**.  
- Experiment with **GitHub Environments** (staging vs production).  

---

✨ Built with ❤️ while learning **DevOps & Cloud**.  
