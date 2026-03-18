# 🌐 Hosting a Static Website on AWS using S3 & Route 53

## 📌 Project Overview
This project demonstrates how to deploy a highly available and scalable static website using Amazon S3 for storage and AWS Route 53 for domain management. It eliminates the need for traditional web servers by leveraging cloud infrastructure.

---

## 🚀 Live Demo
🔗 https://lamusree.github.io/aws-static-website/

---

## 🏗️ Architecture
The solution follows a cloud-based architecture:
- Amazon S3 bucket stores static website files
- S3 static website hosting serves content over HTTP
- AWS Route 53 manages DNS and routes traffic to the S3 endpoint

---

## ⚙️ Technologies Used
- **Amazon S3** – Static website hosting  
- **AWS Route 53** – DNS management  
- **HTML5 & CSS3** – Frontend development  

---

## 🛠️ Implementation Steps

### 1️⃣ Create S3 Bucket
- Create a bucket with a globally unique name (e.g., `lamusree-static-website`)
- Disable **Block all public access**
- Enable static website hosting

### 2️⃣ Upload Website Files
- Upload `index.html` and other assets
- Ensure all files are publicly accessible

### 3️⃣ Configure Bucket Policy
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadAccess",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::lamusree-static-website/*"
    }
  ]
}
```

### 4️⃣ Enable Static Website Hosting
- Set **Index document**: `index.html`
- (Optional) Set **Error document**: `error.html`
- Copy the S3 website endpoint URL

### 5️⃣ Configure Route 53
- Register or use an existing domain
- Create a hosted zone
- Add an **A record (Alias)** pointing to the S3 endpoint

---

## 🔐 Security Considerations
- Follow the principle of least privilege (IAM policies)
- Avoid storing sensitive data in public S3 buckets
- Enable access logging and monitoring
- Consider using AWS CloudFront for HTTPS support

---

## 📊 Key Features
- Highly scalable and reliable hosting
- Cost-effective solution (pay-as-you-go)
- Simple deployment and maintenance
- Fully managed AWS infrastructure

---

## 📸 Screenshots
_Add screenshots of:_
- S3 bucket configuration  
- Static website hosting enabled  
- Bucket policy  
- Route 53 DNS setup  

---

## 🎯 Learning Outcomes
- Understanding AWS S3 static website hosting  
- Configuring DNS using Route 53  
- Managing permissions and public access  
- Deploying real-world cloud-based applications  

---

## ✅ Conclusion
This project demonstrates how AWS services like S3 and Route 53 can be integrated to build a scalable, reliable, and cost-efficient static website hosting solution suitable for modern web applications.

---

## 📎 References
- AWS Official Documentation  
- Amazon S3 User Guide  
- Route 53 Developer Guide  

---

## 👤 Author
**Lamu Sree**  
GitHub: https://github.com/lamusree
