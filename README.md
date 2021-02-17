# Use terraform to provision an NGINX server using Docker  #


**Prerequisites:**  

- Windows 10 machine  
- Docker up and running  
- Terraform up and running  

Source: [https://learn.hashicorp.com/tutorials/terraform/install-cli#quick-start-tutorial](https://learn.hashicorp.com/tutorials/terraform/install-cli#quick-start-tutorial)  
  
**Procedure:**   
From Git bash (or powershell):  

1. Clone repository
1. `cd terraform-docker-demo`
1. Check Terraform configuration file main.tf
2. Initialize the project by running   `terraform init`   . This will download a plugin that allows Terraform to interact with Docker.
1. Provision the NGINX server container with apply. When Terraform asks you to confirm type yes and press ENTER.Run:   
 `terraform apply`  
Verify the existence of the NGINX container by visiting **localhost:8090** (port specified in main.tf) in your web browser or running docker ps to see the container.
<img src="https://github.com/Kari-sad/terraform-docker-demo/blob/master/nginx.JPG">  

1. To view the created container, run `docker ps` 
1. To stop the container, run `terraform destroy`.


You've now provisioned and destroyed an NGINX webserver with Terraform.
