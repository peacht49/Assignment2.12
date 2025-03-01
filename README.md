# Assignment2.12

1. What is the purpose of the execution role on the Lambda function?
It is an IAM role grants the function necessary permissions to access AWS resources when executed/


2. What is the purpose of the resource-based policy on the Lambda function?
Resource based policies are attached directly to the function and authorises access and actions identities can perform. This is useful when we want to manage resource access without modifying identity permissions. Also, when services are used to invoke lambda resource based policies are great fir managing these actions.


3. If the function is needed to upload a file into an S3 bucket, describe (i.e no need for the actual policies)
    - What is the needed update on the execution role? 
      We need to add an execution role to allow the necessary actions, s3:PutObject in this case
    - What is the new resource-based policy that needs to be added (if any)?
      Resource based policies are needed if uploads have to be done from another aws service/s3 bucket