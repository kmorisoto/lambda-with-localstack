# lambda-with-localstack
Lambdaをlocalstackで試す

```shell
docker compose up -d
```

```shell
cd terraform/
terraform init
terraform plan
terraform apply
cd ../
```

```shell
aws  --endpoint-url=http://localhost:4566 lambda invoke --function-name my-function out --log-type Tail --query 'LogResult' --output text |  base64 -d
```
