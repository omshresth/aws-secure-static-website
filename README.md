# Secure Static Website on AWS (S3 + CloudFront)

This project demonstrates how to deploy a **secure, production-ready static website** using AWS services while following **cloud security best practices**.

---

## 🏗 Architecture

User  
→ Amazon CloudFront (Global CDN, HTTPS)  
→ Private Amazon S3 Bucket  

Only CloudFront is allowed to access the S3 bucket using **Origin Access Control (OAC)**.

---

## ☁️ AWS Services Used

- Amazon S3 – Static website storage (private bucket)
- Amazon CloudFront – Content Delivery Network (CDN)
- IAM (S3 Bucket Policy) – Least-privilege access control
- HTTPS (TLS) – Secure content delivery

---

## 🔐 Security Implementation

- S3 bucket is **not publicly accessible**
- Access restricted to CloudFront using **Origin Access Control (OAC)**
- Bucket policy allows **read-only access** to a specific CloudFront distribution
- HTTPS enforced for all viewer requests

---

## 🚀 Deployment Steps (High Level)

1. Created a private S3 bucket and uploaded static website files  
2. Enabled static website hosting for routing configuration  
3. Created a CloudFront distribution with S3 as origin  
4. Configured Origin Access Control (OAC)  
5. Applied least-privilege bucket policy  
6. Set default root object for seamless access  

---

## 🧠 Key Learnings

- Difference between **public S3 hosting vs secure CloudFront hosting**
- Importance of **OAC over legacy OAI**
- How CDN caching improves performance and scalability
- Real-world AWS security and cost-control practices

---

## 📌 Notes

This project was deployed, tested, and later disabled to avoid unnecessary AWS charges.

---

## 👤 Author

**Om Shresth**  
AWS Cloud Learner | Solutions Architect (Aspirant)
