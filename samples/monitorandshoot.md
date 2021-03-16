# Monitoring and Troubleshooting questions samples

- You have configured a CloudWatch alarm to trigger when CPU rises above 60% CPU is currently at 80%.
  What is the status of the alarm ?
  1. ❌ OK
  2. ✅ ALARM
  3. ❌ INSUFFICIENT DATA
  4. ❌ INSUFFICIENT CPU

- Your application is trying to upload a **6GB** file to Amazon S3 and receives a message that "Your proposed **upload exceeds the maximum allowed object size**".
  What is a possible solution for this problem ?
  1. ❌ None; S3 objects are limited 5GB
  2. ✅ Use the multi-part upload API for this object
  3. ❌ Use the large object upload API for this object
  4. ❌ Contact support to increase your object size limit
  5. ❌ Upload to a different region

- Which of these is a true statement ? 
  The AWS error "**InternalError**": We encountered an internal error. **Please try again**".
  means ...
  1. ✅ This is a 500 service-level type error
  2. ❌ This is a 400 client level error
  3. ❌ This is a S3 service error. Resolve for S3
  4. ❌ This is a customer error

- You are writing to a DynamoDB table and received the following exception: *ProvisionedThroughputExceededException*.
  However, according to your CloudWatch metrics for the table, you are not exceeding your provisioned throughput.
  What could be an explanation for this ?
  1. ❌ You haven't provisioned enough DynamoDB storage instance
  2. ❌ You're exceeding your capacity on a particular Range Key
  3. ✅ You're exceeding your capacity on a particular Partition Key
  4. ❌ You're exceeding your capacity on a particular Sort Key
  5. ❌ You haven't configured DynamoDB Auto Scaling triggers

- What happens, by **default**, when one of the ressources in an AWS CloudFormation stack cannont be created ?
  1. ❌ Previously created ressources are kept, but the stack creation is terminated
  2. ✅ Previously created ressources are deleted, and the stack creation is terminated
  3. ❌ The stack creation continues, and the final results indicate which steps failed
  4. ❌ AWS CloudFormation  templates are parsed in advance so that stack creation is guaranteed to succeed

- You have received a "404 NOT FOUND: NoSuchBucket" error code response.
  What does this error code mean ?
  1. ❌ S3 cannot find bucket named: NoSuchBucket
  2. ✅ S3 cannot locate the requested Bucket
  3. ❌ S3 object is not available
  4. ❌ S3 service is temporarily unavailable. Retry