# Serverless application developmenet accounts uploads processing

template show's the fallowing steps

1. Upload account creation file to S3
2. Notify SNSTopic with upload files information(meta data)
3. SNSTopic will send message to SQSQueue
4. Lambda function1 will pick message from SQSQueue and update metadata information into DynamoDB
5. Lambda fucntion2 will call DynamoDB with API call and get the information about upload file
6. Lambda fucntion2 will download the file from S3 and upload account information into RDS DB.



