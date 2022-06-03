# Deploying-a-Static-Website-on-AWS

## Project Overview
This project focuses on:

 1. Hosting a static website on S3
 2. Accessing the cached website pages using CloudFront content delivery network (CDN) service. Keep in mind that CloudFront offers low latency and high transfer speeds during website rendering. 

NB: This was one of my Udacity DevOps Nanodegree projects assigned to me.

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
![udacity new](https://user-images.githubusercontent.com/89241109/171459694-324bc10b-c77d-4bb7-a185-ab57af7f197b.png)

### Step 3: Securing bucket via IAM
For static website hosting, it is required to make buckets public
![udacity new 3](https://user-images.githubusercontent.com/89241109/171460071-0929de23-5a74-4386-a680-c69daae2df58.png)

### Step 4: Configuring S3 bucket
I enabled static website hosting and made the contents of the index.html file publicly readable so that it can be accessed at the website endpoint
![udacity 2](https://user-images.githubusercontent.com/89241109/171462570-5d75c3f2-0ca6-4cfd-bc4c-fbee88db2fc8.png)
![udacity new 4](https://user-images.githubusercontent.com/89241109/171461023-d934f3fe-ef6d-49ca-9f6d-0f865c71cbe8.png)

### Step 5: Distributing Website via CloudFront

I created a CloudFront distribution which attached to the S3 and S3 caching pages
![cloudfront2](https://user-images.githubusercontent.com/89241109/171464477-de85a737-eaa4-4c87-ad34-f4dec36ecf87.png)

![cloudfront](https://user-images.githubusercontent.com/89241109/171464456-19a88dd8-d376-40c0-bd2c-58f459d242d6.png)

### Step 6: Accessing website in web browser
Pasting the CloudFront domain name in a web browser even without the index.html at the end displayed the content of the default home page
![websiteCloudfront](https://user-images.githubusercontent.com/89241109/171468273-ccfe0319-bb0a-4e58-871d-086a46115bc8.png)

Also, the website can also be accessed through the website-endpoint and S3 object URL
![websiteS3](https://user-images.githubusercontent.com/89241109/171465679-ff3e4d92-5e81-489f-a9f7-905c782d055d.png)

NB: The bucket was made public because it is being hosted on S3, if it wasn't the bucket would have been made private and hosted on the CloudFront domain name which wouldn't allow the private content to be accessible through S3 object URL and website-endpoint.





