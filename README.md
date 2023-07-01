# deploy-fargate-ecs-apps-infrastructure-aws-with-terraform

### Commands

1. terraform init -backend-config="infrastructure-prod.config"
2. terraform plan -var-file="production.tfvars"
3. terraform apply -var-file="production.tfvars" auto-approve

### Pipeline

1. Build stage - sh deploy.sh build
2. Dockerize app - sh deploy.sh dockerize and push to ECR
3. Deploy App to ECS fargate - sh deploy.sh deploy
