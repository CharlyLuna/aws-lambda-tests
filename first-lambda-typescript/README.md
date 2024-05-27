# First test creating a lambda function with typescript

To create the lambda follow the next steps:

Run the build to transpile the ts code and create the zip file

```
npm run build
```

Create the lambda using the zip

```
aws lambda create-function --function-name hello-world --runtime "nodejs18.x" --role arn:aws:iam::123456789012:role/lambda-ex --zip-file "fileb://dist/index.zip" --handler index.handler
```

#### Note: the role must be created on your aws account and the two basic policies that it needs are **AWSLambdaBasicExecutionRole** and **AWSXRayDaemonWriteAccess**.
