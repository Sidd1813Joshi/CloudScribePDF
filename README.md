# CloudScribePDF – Serverless PDF Utility (AWS Lambda + S3 + API Gateway)

A fully serverless PDF utility inspired by ILovePDF, built using AWS Lambda, Amazon S3, and API Gateway.
This system allows users to securely upload PDF files using Pre-Signed URLs and perform operations like Merge, Split, and Compress — all without exposing any AWS credentials.

## Features
🔐 Secure PDF uploads using S3 Pre-Signed URLs

🧩 Supports Merge, Split, and Compress operations

⚡ Fully serverless backend using AWS Lambda

📦 UUID-based file storage for collision-free uploads

🌐 Clean and simple frontend interface

🔁 Automatic processing and output delivery via S3

### Tech Stack
AWS Lambda (Python) – Backend processing

Amazon S3 – Secure storage for input/output PDFs

API Gateway – POST endpoint for Lambda invocation

Pre-Signed URLs – Secure client-side uploads

HTML, CSS, JavaScript – Lightweight frontend

Python PDF libraries – For merge, split, and compression

#### Project Architecture
User Frontend
     │
     ▼
API Gateway (POST Request)
     │
     ▼
AWS Lambda 
  ├── Generates Pre-Signed URL
  ├── Handles Upload Metadata
  └── Processes (Merge | Split | Compress)
     │
     ▼
Amazon S3
  ├── uploads/ (input PDFs)
  └── outputs/ (processed PDFs)
     │
     ▼
User downloads final PDF
