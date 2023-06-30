# deploy-fargate-ecs-apps-infrastructure-aws-with-terraform

### Commands

terraform init -backend-config="infrastructure-prod.config"
terraform plan -var-file="production.tfvars"
terraform apply -var-file="production.tfvars" auto-approve

### Pipeline

Build stage - sh deploy.sh build
Dockerize app - sh deploy.sh dockerize and push to ECR
Deploy App to ECS fargate - sh deploy.sh deploy