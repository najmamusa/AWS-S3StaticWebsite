# AWS S3 Static Website Hosting Tutorial
Welcome! If you're looking to get a static website up and running with minimal fuss, you're in the right place. This guide is designed for anyone, especially beginners, to host their website on Amazon Web Services (AWS) S3 with ease.

## Description 
This repository simplifies the process of hosting a static website using AWS S3. Static websites are great for portfolios, blogs, and landing pages because they are fast, secure, and cost-effective. AWS S3, known for its reliability and scalability, offers a straightforward way to make your website accessible to the world.

## What You'll Learn:
How to create an AWS S3 bucket configured for website hosting.
Uploading your static website files (HTML, CSS, JavaScript) to your S3 bucket.
Setting up the necessary permissions to make your website publicly accessible.
Optional: Configuring a custom domain for your S3-hosted website.


## Prerequisites:
An AWS account.
Basic knowledge of HTML/CSS (if you're creating your website from scratch).
Your static website files ready to upload.


## Summary:
- Set Up Your AWS Account: If you haven't already, sign up for AWS.
- Create an S3 Bucket: We'll guide you through creating and configuring your bucket for web hosting.
- Upload Your Files: Get your HTML, CSS, and JavaScript files onto AWS S3.
- Make It Public: Adjust the bucket settings to serve your website to the world.
- Visit Your New Website: Access your site through the unique S3 endpoint.

**1. Set Up Your AWS Account:**
- Sign Up for AWS: Visit the AWS website and click on the "Create an AWS Account" button.
- Provide Account Information: Enter your email address, password, and AWS account name. Follow the on-screen instructions to complete the sign-up process.
- Verify Your Identity: AWS will ask for your phone number to verify your identity. Enter your phone number and follow the verification steps.
- Choose a Support Plan: Select the "Basic" plan, which is free. You won't be charged unless you choose a paid plan or use paid services beyond the free tier limits.
- Payment Information: You'll need to provide a valid credit card to create an AWS account, even for the free tier. However, you won't be charged unless you exceed the free tier limits.

 **2. Create an S3 Bucket:**
Go to the S3 Console: Sign in to the AWS Management Console and navigate to the S3 service.
- Create a Bucket: Click on the "Create bucket" button.
- Enter Bucket Details: Provide a unique name for your bucket. Bucket names must be globally unique across all of AWS, so choose a name that is not already in use.
- Choose Region (optional): Select the AWS region closest to your target audience for better performance.
- Configure Options: Leave the default settings for now and proceed to create the bucket.

**3. Enabling static website hosting:**
![Capture 2](https://github.com/najmamusa/AWS-S3StaticWebsite/assets/110435863/9cec172e-347e-4df7-b1ac-dd068dbe3639)
- Under the properties section of the S3 bucket we have just created. navigate to the static website hosting section and press Edit.
- Enable the static website hosting option.
- For the index document, input 'index.html' for this project. This document will be the HTML file for our static website.
- Do not change anything else on this page and save changes at the bottom of the page.

**4. Endpoint address:**
- After enabling the static website hosting, you should have an endpoint link under the same section in properties.
- This endpoint will be the address where we will be hosting our static website.
- If you open the link in another tab, you should see the following error:
  ![Capture 3](https://github.com/najmamusa/AWS-S3StaticWebsite/assets/110435863/8182bebf-ab98-426a-8e66-23945b9483ca)

**5. Enabling Public Access:**
  - This error we are receiving is due to the blocking of public access.
  - To change this, navigate to the permissions section of the bucket and under Block Public Access, select Edit.
  ![Capture 4](https://github.com/najmamusa/AWS-S3StaticWebsite/assets/110435863/85182b7e-e28a-466f-aece-0a00fb9fdf53)
  - Deselect the block all public access section.
  - As there are some risks to enabling public access, there will be some warnings, but confirm all warnings.

**6. Bucket Policy**
  - Under the same section, scroll to the Bucket Policy and press Edit.
  - Here, enter the contents of the JSON file attached to this repo as a template, replacing the BucketName with yours.
  ![Capture 5](https://github.com/najmamusa/AWS-S3StaticWebsite/assets/110435863/9acf216b-61c0-4e70-84d8-d50358118de9)

 
**7. Uploading File(s):**
 - Now that the bucket can host a publicly accessible static website, we need to insert the index.html file with the code for our simple website.
 - In my example, I have added uploaded an extremely simple index.html file and an image which was attached to the HTML file.
 - A copy of both the file and the image used in this example can be found attached to this repo.
 - Once your files are successfully uploaded, if you refresh the page with the error message, you should now see the following result:
 ![Capture 7](https://github.com/najmamusa/AWS-S3StaticWebsite/assets/110435863/4a69d0b0-86a9-4ce4-a262-dfceb5725261)

**8. Congrats!**
You have successfully hosted a simple static website using AWS S3 Buckets. You can now return to the bucket, empty the bucket and delete it!


![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)

