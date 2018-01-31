## Terraform test cases

How to run one of the Terraform test cases:

* Create a file in the project top dir with name `terraform.tfvars` and the following content:
  ```hcl
  secret_key="<secret_key_data>"
  access_key="<access_key_data>"
  ec2_url="<ec2_url>"
  az="<default_az_name>"
  subnet_id="<default_subnet_id>"
  ```
* Navigate to the case directory, for example 'cases/run_instance_with_cdrom':
  ```sh
  $ cd cases/run_instance_with_cdrom
  ```
* Create a symlink to the `terraform.tfvars` file:
  ```sh
  $ ln -s ../../terraform.tfvars
  ```
* Run Terraform `plan` and `apply` commands:
  ```sh
  $ terraform plan
  $ terraform apply
  ```