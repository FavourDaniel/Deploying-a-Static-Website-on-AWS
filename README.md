# Deploying-a-Static-Website-on-AWS

## Project Overview
This project focuses on

 1. Hosting a static website on S3
 2. Accessing the cached website pages using CloudFront content delivery network (CDN) service. Keep in mind that CloudFront offers low latency and high transfer speeds during website rendering.

**The steps I took to achieve this**:
- Creating a public S3 bucket and upload the website files to your bucket.
- Configuring the bucket for website hosting and secure it using IAM policies.
- Speeding up content delivery using AWS’s content distribution network service, CloudFront.
- Ensuring the website is accessible in a browser using the unique CloudFront endpoint.

### Prerequisites for this project are:
 1. An AWS account
 2. Website (any language)

## Detailed steps on how this was achieved
### Step 1: Creating an S3 bucket
Navigating to Amazon S3 from the AWS management console, I created an s3 bucket to store my website files. I also allowed public access so that the website could be accessed from anywhere on the net.
![screenshot-2021-01-12-at-6 32 23-pm](https://user-images.githubusercontent.com/89241109/171367150-598a1895-af16-4759-8f5f-eba9326d8ab7.png)
![udacity 3 (2)](https://user-images.githubusercontent.com/89241109/171366860-01320d80-b3ac-4f86-9140-d7007a153723.png)

### Step 2: Uploading website files
After creating the s3 bucket, I uploaded the website files into it. 






