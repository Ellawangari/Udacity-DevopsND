# Project Overview

Hosting a static website on S3 and
Accessing the cached website pages using CloudFront content delivery network (CDN) service. Recall that CloudFront offers low latency and high transfer speeds during website rendering.
Note that Static website hosting essentially requires a public bucket, whereas the CloudFront can work with public and private buckets.

# Step 1 : Create a S3bucket
![alt text](https://github.com/Ellawangari/Udacity-DevopsND/blob/main/imgs/1.PNG)

# Step 2: Upload files to S3 Bucket
![alt text](https://github.com/Ellawangari/Udacity-DevopsND/blob/main/imgs/2.PNG)

# Step 3: Secure Bucket via IAM
![alt text](https://github.com/Ellawangari/Udacity-DevopsND/blob/main/imgs/3.PNG)

# Step 4 : Configure S3 Bucket

![alt text](https://github.com/Ellawangari/Udacity-DevopsND/blob/main/imgs/4.PNG)

# Step 5: Distribute Website via CloudFront

![alt text](https://github.com/Ellawangari/Udacity-DevopsND/blob/main/imgs/5.PNG)

# Step 6: Access Website in Web Browser
 1. Open a web browser like Google Chrome, and paste the copied CloudFront domain name (such as, dgf7z6g067r6d.cloudfront.net) without appending /index.html at the end. The CloudFront domain name should show you the content of the default home-page.
 
 ![alt text](https://github.com/Ellawangari/Udacity-DevopsND/blob/main/imgs/6.PNG)
 
 2. Access the website via website-endpoint.
 ![alt text](https://github.com/Ellawangari/Udacity-DevopsND/blob/main/imgs/7.PNG)
 
 3. Access the bucket object via its S3 object URL.
  ![alt text](https://github.com/Ellawangari/Udacity-DevopsND/blob/main/imgs/8.PNG)
 
 
 
