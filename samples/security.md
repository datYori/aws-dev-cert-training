# Security questions samples

- In AWS, which security aspects are the **customer's responsibility** ? (Choose four answers.)
  1. ✅ Life-cycle management of IAM credentials
  2. ❌ ~~Decommissioning storage devices~~
  3. ✅ Security Group and ACL (Access Control List) settings
  4. ✅ Encryption of EBS (Elastic Block Store) volumes
  5. ❌ ~~Controlling physical access to compute resources~~
  6. ✅ Patch management of EC2 instances 


- You created a message queuing application with Amazon SQS and enabled server-side encryption to encrypt the message body sensitive data. Which service will **allow you** to **manage and rotate your encryption keys centrally** ?
  1. ❌ ~~Amazon SQS does not support SSE~~
  1. ✅ AWS KMS Customer Master Key
  1. ❌ ~~AWS IAM~~
  1. ❌ ~~AWS KMS Default Master Key~~

- Which of the following **request headers**, when specified in an **API call**, will cause an object to be encrypted by **SSE**
  1. ❌ ~~server-side encryption~~
  1. ❌ ~~AES256~~
  1. ❌ ~~amz-server-side-encryption~~
  1. ✅ x-amz-server-side-encryption

- Games-R-Us is launching a new game app for mobile devices. **Users log in to the game** using their existing **Facebook account** and the game records player data and scoring information directly to an Amazon Dynamp DB table. What is the **most secure approach for signing requests** to DynamoDB API ?
  1. ❌ ~~Create an IAM user with access credentials that are distributed with the mobile app to sign the requests~~
  1. ❌ ~~Distribute the AWS root account access credentials with the mobile app to sign the requests~~
  1. ✅ Request temporary security credentials using web identity federation to sign the requests
  1. ❌ ~~Establish cross account access between the mobile app and the DynamoDB table to sign the requests~~