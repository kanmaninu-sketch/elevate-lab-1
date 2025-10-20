# elevate-lab-1

#  AWS S3 Bucket Static Website Hosting

This project demonstrates how to host a static website using Amazon S3. It includes uploading a `.txt` file, configuring bucket policies, and enabling static website hosting.

##  Bucket Setup

- **Bucket Name**: `elevatelab1`
- **Region**: `Asia Pacific (Mumbai) ap-south-1`
- **File Uploaded**: `elevatelab1.txt`
##  Steps to Deploy

1. **Create an S3 Bucket**
   - Go to AWS S3 Console.
   - Create a new bucket with a unique name.
   - Uncheck "Block all public access" to allow public access.

2. **Upload Files**
   - Upload your `elevatelab1.txt` or other static files.

3. **Set Bucket Policy**
   - Go to **Permissions > Bucket Policy** and paste the following:
   ```json
   {
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "statement1",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:getobject",
            "Resource": "arn:aws:s3:::elevatelab1/*"
        }
    ]
}

4. **Enable Static Website Hosting**
  - Go to Properties > Static Website Hosting.
  - Choose "Enable".
  - Set the Index document to elevatelab1.txt .
  - Save changes.

5. **Access Your Website**
  - After enabling hosting, AWS provides a Website Endpoint URL.
  - URL: http://elevatelab1.s3-website.ap-south-1.amazonaws.com
  - Open this URL in your browser to view the hosted file.
