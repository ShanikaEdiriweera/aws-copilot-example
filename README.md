## AWS Copilot CLI Sample App

This is a sample AWS Copilot sample app. You can use AWS Copilot to deploy this simple website to Amazon ECS. 

## Deploying 

To deploy this app, clone this repo and then run:

```
copilot app init --domain <domain>
copilot init # init service1, test env and deploy
copilot svc init
copilot svc deploy --name service2 --env test
copilot env init
copilot env deploy --name dev
copilot svc deploy --name service1 --env dev
copilot svc deploy --name service2 --env dev
opilot pipeline init -u https://github.com/ShanikaEdiriweera/aws-copilot-example -b main -n test-app-pipeline -p Workloads -e test,dev
copilot pipeline deploy
```

Copilot will set up the following resources in your account:
* A VPC
* Subnets/Security Groups
* Application Load Balancer
* Amazon ECR Repositories
* ECS Cluster & Service running on AWS Fargate
* Route53 DNS Records
* ACM Certificates
* CodePipeline

## Cleaning up

Since this demo sets up resources in your account, let's delete them so you don't get charged: 

```
copilot app delete
```

## Learning More

If you want to learn more about AWS Copilot, check out our [documentation](https://aws.github.io/copilot-cli/).

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

