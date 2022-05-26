# Output PDF file in Japanese Api with AWS Lambda , API Gateway, ECR.


## Usage

### Setup

Create .envrc file.
```shell
touch .envrc
```

Write environment variables, and set variables.
```shell
echo "export APP_NAME=random-letter" >> .envrc
echo "export ACCOUNT_ID=00000000000" >> .envrc
echo "export PROFILE=default" >> .envrc
echo "export REGION=ap-northeast-1" >> .envrc
echo "export REGION=ap-northeast-1" >> .envrc
direnv allow
```

### Build Image 

```shell
make build-dev
```

### Confirm in local

Run
```shell
make run-local
```

Confirm in other shell.
```shell
curl -XPOST "http://localhost:9000/2015-03-31/functions/function/invocations" -d '{}'
```

### Push Image
```shell
make push-dev
```

### Create AWS Lambda Function
[参考](https://aws.amazon.com/jp/blogs/aws/new-for-aws-lambda-container-image-support/)