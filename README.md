# assignment2-12
Given a Lambda function that is triggered upon the creation of files in an S3 bucket, answer the following:

Q1. What is the purpose of the execution role on the Lambda function?

Excution role in AWS Lambda are IAM roles that grant permission for the function to access AWS services and resources during its excution

Q2. What is the purpose of the resource-based policy on the Lambda function?

A resource-based policy on a Lambda function controls which AWS services or other accounts can invoke the function. Acting as a security mechanism to limit who can access and run the Lambda code.

Q3. If the function is needed to upload a file into an S3 bucket, describe (i.e no need for the actual policies)
     - What is the needed update on the execution role?
     The following permission is needed s3:PutObject in the execution role
     - What is the new resource-based policy that needs to be added (if any)?
     It policy must allow S3 to invoke the function. The policy would specify that the S3 bucket has permission to invoke the Lambda function, since the create of files will trigger the Lambda function in the first place, therefore, no additional rule is needed to be added.
