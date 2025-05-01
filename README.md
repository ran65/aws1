[rahaf-alrajeh.zip](https://github.com/user-attachments/files/20000229/rahaf-alrajeh.zip)
Rahaf Alrajeh
SDA1013 part1
I created a new bucket named rahaf-clarusway in the eu-north-1 region.

Uploaded the following files to the root of the bucket:
index.html
logo.png
sda.png

Enabled static website hosting
Index document: index.html

Added the following Bucket Policy to allow public access to all files:
json
CopyEdit
{
  "Version": "2012-10-17",
  "Statement": [{
    "Effect": "Allow",
    "Principal": "*",
    "Action": "s3:GetObject",
    "Resource": "arn:aws:s3:::rahaf-clarusway/*"
  }]
}


Opened the S3 website and take screenshoot
curl -I http://rahaf-clarusway-assets.s3-website-eu-north-1.amazonaws.com
Got the expected 200 OK response.

Part2
Created a Launch Template using Amazon Linux.
Make sure the number of VPC is the same one that am working on.

Create target group.

Create load balancer.

Configure Auto Scaling Group with specific settings such as max=3 , min=1 and desired=2.

Create security group and add rules.

Check instances. 

Part3 

Create Internet facing ALB with HTTP listener on port 80
Registered ASG instances in the Target Group
Copied the web link from load balance and check if it’s open and take screenshoot.
Curl the link .
<img width="1440" alt="ASG details" src="https://github.com/user-attachments/assets/452abb61-78e5-48ca-b485-f51884eb3ce7" /><img width="908" alt="final web" src="https://github.com/user-attachments/assets/e438440f-ae6a-4b10-b750-261893959bcf" />
<img width="915" alt="part1 web page" src="https://github.com/user-attachments/assets/89ec07ea-51e5-4721-949a-80d4a9682cae" />

<img width="586" alt="pa<img width="1440" alt="running instance " src="https://github.com/user-attachments/assets/6d6001f1-65b6-4f00-b5b7-33b7d6f42886" />
rt1 curl" src="https://github.com/user-attachments/assets/43e460e1-40ec-466f-a905-82744321a95d" />

