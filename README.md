# Deploy to S3/Cloudfront
In this guide, you will learn how to deploy your tezjs site to AWS3/Cloudfront Hosting.

## Deployed Url:
https://d3kv2tw1u0hreu.cloudfront.net/

## Preparing for deployment:
Run the following command to create tezjs project:
  - `npm create tez@latest`
  - `cd [projectName]`
  - `npm install` - for installing the required dependencies
  - `npm run build` - for build the project
  - `npm run dev` - for run the project

## Pre-requisites
Make sure you have:
  - AWS account
  - AWS-Cli install.
  - IAM-Account needed with s3 and cloudfront permission.
  - AWS need to configure.
## Deployment:
Go to https://aws.amazon.com/amplify/console/ to get started.
1. Create a S3 Bucket.
2. Create a Cloufront which have a reference of bucket that you have see in previouse step.
3. Copy the dist to S3 bucket by using console or given aws-cli command 
  `aws s3 cp dist/* [s3uri] --recursive`
2. Create one purge or invalidation in Cloudfront service of path `/*`
  
## Reference link:
- [Deploy static site using s3 and cloudfront](https://aws.amazon.com/premiumsupport/knowledge-center/cloudfront-serve-static-website/#:~:text=To%20serve%20a%20static%20website%20hosted%20on%20Amazon%20S3%2C%20you,with%20anonymous%20(public)%20access%20allowed)
- [AWS-Cli install]( https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html )

