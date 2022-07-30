Deploy Static Website on AWS

In this project, you will deploy a static website to AWS using S3, CloudFront, and IAM.

The files included are: 

index.html - The Index document for the website.
/img - The background image file for the website.
/vendor - Bootssrap CSS framework, Font, and JavaScript libraries needed for the website to function.
/css - CSS files for the website.


## This is the first project of Udacity Cloud Devops Nanodegree Program.

Problem Statement:

In this project I need to deploy a static website in AWS s3. Then it should be distributed By CloudFront. Finnaly Route53 should be used as DNS service
The index.html and images files are provided in the project repository

Solutions:


Create,configure and deploy contentsto S3 bucket:

1. open the console in Aws and create a user with IAM policy( Policy should provide access to s3 )
2. Login as the user created and create a S3 bucket with Globally unique Name.( s3 bucket Name is ****)
3. Node down the name of S3 bucket and use it as bucket name as ENV variables in Circle CI
4. Use the Access key and Sercret access key of AWS as the Enviornment Variables in Circle ci
5. Here used the Circle CI config file to deploy the files in s3 bucket

Cloud Front:

1. Configure a new distribution and linked it with existing bucket. 
2. Bucket policy is created by OAI
3. redirect HTTP requests to HTTPS

output link https://d1bzicvpv9s8zw.cloudfront.net
static-website endpoint http://udacityproject-1byalmamun.s3-website-us-east-1.amazonaws.com


