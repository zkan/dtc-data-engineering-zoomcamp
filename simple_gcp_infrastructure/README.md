```sh
# Refresh service-account's auth-token for this session
gcloud auth application-default login

# Initialize state file (.tfstate)
terraform init

# Check changes to new infra plan
terraform plan -var="project=<your-gcp-project-id>"
```

```sh
# Create new infra
terraform apply -var="project=<your-gcp-project-id>"
```

```sh
# Delete infra after your work, to avoid costs on any running services
terraform destroy
```

```sh
terraform plan -var="project=dtc-de-course-350414" -out tfplan
terraform apply "tfplan"
terraform destroy -var="project=dtc-de-course-350414"
```
