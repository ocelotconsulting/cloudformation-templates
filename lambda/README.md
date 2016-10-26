## lambda-cloudformation
This small template can be used to create a lambda function from a file which has been uploaded to S3

## Parameters
Prior to execution, edit the [parameters file](parameters.json) to populate the needs for CloudFormation.

| *Parameter*                 | *Description*         |
| :--------------------- |:--------------|
| `LambdaNameParameter`            | The name for the lambda function as well as part of the inline policy name in the IAM role.  |
| `LambdaHandlerNameParameter`            | The name of the handler function for the lambda to execute.  |
| `LambdaMemoryParameter`            | The amount of memory to allocate to the lambda function.  |
| `LambdaRuntimeParameter`            | The name of the lambda runtime to assign to this function (Valid Values: `nodejs` | `nodejs4.3` | `java8` | `python2.7`).  |
| `LambdaBucketParameter`            | The name of the S3 bucket containing the lambda code.  |
| `LambdaFileParameter`            | The file for using with the lambda function.  |


## Execution
      $ aws cloudformation create-stack --stack-name stacksonstacks --template-body file:///local/path/to/lambda_cft.json --parameters file:///local/path/to/parameters.json --capabilities CAPABILITY_IAM
