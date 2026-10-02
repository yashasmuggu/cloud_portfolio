[README.md](https://github.com/user-attachments/files/32953002/README.2.md)
# Cloud Portfolio – AWS S3 + CloudFront

A responsive single-page portfolio deployed on AWS using Amazon S3 and Amazon CloudFront with HTTPS.

## 🌐 Live Website

dxkekm1rj0c1d.cloudfront.net

## 📦 GitHub Repository

https://github.com/yashasmuggu/cloud_portfolio

## 🛠️ Technologies Used

- HTML5
- CSS3
- Google Fonts
- Font Awesome
- Git & GitHub
- Amazon S3
- Amazon CloudFront
- CloudFront Origin Access Control (OAC)
- HTTPS

## 📁 Project Structure

```text
cloud_portfolio/
├── index.html
├── style.css
└── assets/
```

## ☁️ AWS Deployment

### 1. Create S3 Bucket

An S3 bucket named `yash-cloud-portfolio-2026` was created in the AWS Europe (Stockholm) region.

### 2. Upload Website Files

The portfolio files were uploaded to the S3 bucket:

- `index.html`
- `style.css`
- `assets/`

### 3. Configure Static Website Hosting

S3 static website hosting was enabled with:

- Index document: `index.html`

### 4. Configure CloudFront

A CloudFront distribution was created using the S3 bucket as the origin.

Configuration includes:

- Default root object: `index.html`
- Origin Access Control (OAC)
- Cache policy: `CachingOptimized`
- Allowed methods: `GET, HEAD`
- Viewer protocol policy: `Redirect HTTP to HTTPS`

### 5. HTTPS

CloudFront provides the final HTTPS endpoint:

https://dxkekm1rj0c1.cloudfront.net

HTTP requests are redirected to HTTPS.

## 🔐 Security

CloudFront Origin Access Control (OAC) is used so that CloudFront can access the S3 objects through the configured distribution.

The S3 bucket policy permits `s3:GetObject` to the CloudFront service principal for the specific CloudFront distribution.

## 🔄 Deployment Workflow

```text
Local Portfolio
      ↓
   GitHub
      ↓
   Amazon S3
      ↓
CloudFront + OAC
      ↓
 HTTPS Website
```

## 🎯 Task Objective

This project was completed as part of the **Cloud Computing & DevOps – Task 1** assignment. The objective was to build and deploy a static portfolio using Amazon S3 and serve it through CloudFront with HTTPS.

## 👤 Author

**Yashas Muggu**
