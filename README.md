# atc

Steps to Deploy

1. Clone the repository with the Dockerfile, Terraform code, and Kubernetes files.
2. Set up your AWS credentials for Terraform and configure your environment for the AWS region.
3. Run Terraform to provision the infrastructure:
```
terraform init
terraform apply
``` 
4. Build and push the Docker image
```
docker build -t your-dockerhub-username/web-app-apache .
docker push your-dockerhub-username/web-app-apache
``` 
5. Deploy Kubernetes resources:
```
kubectl apply -f deployment.yaml
kubectl apply -f monitoring.yaml
``` 
6. Check the external IP of your web application:
```kubectl get svc web-app-service```


