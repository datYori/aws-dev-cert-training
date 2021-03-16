# Development with AWS questions samples

- You are about to provide an **S3 bucket ressource-based permisssions** so you can grant access to your friend, Boo.
  His AWS **account number** is 123412341234 and his **IAM username is Boo**. What should be the **format for the ARN** ? (Choose four answers.)
  1. ❌ "Principal":{ "AWS": ["arn:aws:s3:123412341234:user/Boo"]}
  2. ✅ "Principal":{ "AWS": ["arn:aws:iam:123412341234:user/Boo"]}
  3. ❌  You cannont do it with a bucket policy. You must create user based permissions in IAM


- You run an ad-supported **photo-sharing website using Amazon S3** to serve photos to visitors of your site.
  At some point, you find out that **other sites are linking to the photos on your site**, causing loss to your business.
  What is an **effective method to mitigate this problem** ?
  1. ❌ Store photos on an EBS volume of the web server
  2. ✅ Remove public read access and use signed URLs with expiry dates
  3. ❌ Use CloudFront distributions for static content
  4. ❌ Block the IPs of the offfending websites in Security Groups

- Which of the following is an example of a good Amazon **DynamoDB partition key schema for provisoned throughput** efficiency ?
  1. ✅ Student ID, where every student has a unique identification number
  2. ❌ College ID, where there are two colleges in the university
  3. ❌ Class ID, where every student is one of four classes
  4. ❌ Tuiton plan, where the vast majority of students are in-state and the rest are out-state

- A security system monitors **3000 cameras** and saves image metadata every **30 seconds** to an AmazonDB table.
  Each sample involves writing **512 bytes of data**. The writes are evenly distributed over time.
  How much write throughput is required for the target table ?
  1. ❌ 30 WCU
  2. ✅ 100 WCU
  3. ❌ 600 WCU
  4. ❌ 300 WCU
  5. ❌ 3600 WCU

    <details>
    <summary>How to solve this</summary>
    <pre>
    - 1 WCU = one write per seconds of 1 KB (1024 bytes)
    - Each sample involves writing 512 bytes so at least 1 WCU is needed
    - Throughput = (3000 * 1 WCU) / 30 secs = 100  WCU / sec 
    </pre>
    </details>

-  When using a **large Scan** operation in DynamoDB, what techniques can you use to **minimize the impact of a scan on table's provisioned throughput** ?
  1. ✅ Set a smaller page size for the scan
  2. ❌ Use paralle scans
  3. ❌ Define a range index on the tables
  4. ❌ Pre warm the table by updating all items

- Company B provides an online image recognition service and uses SQS to decouple system components for scalability.
  **SQS consumers poll the imaging queue as often as possible** to keep end-to-end throughput as high as possible.
  However, **Company B is realizing that polling in tights loops is burning CPU cycles and increasing costs with empty responses**.
  How can Company B reduce the number of empty responses ?
  1. ❌ Set the imaging queue VisibilityTimeout attribute to 20 seconds
  2. ✅ Set the imaging queue Receive Message Wait Time Seconds attribute to 20 seconds
  3. ❌ Set the imaging queue MessageRetentionPeriod attribute to 20 seconds
  4. ❌ Set the DelaySeconds parameter of a message to 20 seconds

- What is the **default** settings for SQS **visibility timeout** ? 
  1. ✅ Thirty seconds
  2. ❌ One minute
  3. ❌ One day
  4. ❌ One week

- You have written an application that uses the Elastic Load Balancing service to spread traffic to several web servers.
  **Your users complain that they are sometimes forced to log in again** in the middle of using your application, after they've already logged in.
  This is not how you except your application to work.
  What is a possible solution to prevent this from happening ?
  1. ❌ Use instance memory to save session state
  2. ❌ Use instance storage to save session state
  3. ❌ Use EBS to save session state
  4. ✅ Use ElastiCache to save session state
  5. ❌ Use Amazon Glacier to save session state

- Which of the following services are key / value stores ? (Choose three answers.)
  1. ✅ Amazon ElastiCache
  2. ❌ Amazon Simple Queue Service
  3. ✅ Amazon DynamoDB
  4. ❌ Amazon Simple Workflow Service
  5. ✅ Amazon Simple Storage Service