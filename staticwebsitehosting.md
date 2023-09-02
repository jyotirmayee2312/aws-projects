---

# Project Documentation: Hosting a Static Website using AWS S3 Bucket

## Introduction

This documentation outlines the steps required to host a static website using Amazon Web Services (AWS) Simple Storage Service (S3) bucket. By following this guide, users will learn how to upload website content to an S3 bucket, configure it for static website hosting, and connect it to a custom domain using AWS Route53.

## Tools Used

- **AWS S3 bucket**
- **AWS Route53**

## Implementation Steps

### Step 1: Create an S3 Bucket

1. Log in to your AWS Management Console.
2. Navigate to the S3 service.
3. Click "Create Bucket."
4. Provide a unique bucket name, choose a region, and click "Next."
5. Configure options and permissions as needed, then click "Next."
6. Review the settings and click "Create Bucket."

### Step 2: Upload Website Content

1. Inside the newly created bucket, click "Upload."
2. Select the website's HTML, CSS, and other files.
3. Configure permissions for uploaded objects, if necessary.
4. Click "Upload" to upload the files to the bucket.

### Step 3: Enable Static Website Hosting

1. In the bucket properties, navigate to the "Static website hosting" section.
2. Choose "Use this bucket to host a website."
3. Set the "Index document" to your main HTML file (e.g., "index.html").
4. Optionally, set the "Error document" for handling 404 errors.
5. Save the changes.

### Step 4: Edit Bucket Policy for Public Access

1. In the bucket properties, navigate to the "Permissions" section.
2. Under "Bucket policy," click "Edit."
3. Add a policy that grants public read access to the bucket's objects.
4. Save the policy changes.

### Step 5: Access Static Website

1. After enabling static website hosting, a website endpoint URL will be provided.
2. Access the website using the provided endpoint URL. Example: http://your-bucket-name.s3-website-region.amazonaws.com.

### Step 6: Connect Custom Domain using AWS Route53

1. Log in to your AWS Management Console.
2. Navigate to the Route53 service.
3. Create a hosted zone for your custom domain.
4. Create a record set within the hosted zone.
5. Choose "Type" as "Alias."
6. Select the S3 bucket that is hosting the static website as the alias target.
7. Save the record set.

## Conclusion

By following the above steps, you have successfully hosted a static website using AWS S3 bucket and connected it to a custom domain using AWS Route53. This setup allows you to serve your static website to users worldwide in a scalable and efficient manner.

---
