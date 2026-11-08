# Terraform / IaaC Advantages
- 1. version control with infra as a code
- 2. Declarative way of creating infra, provided we use right syntax
- 3. Consistent infra --> lower env are ignored then PROD. working inDEV not working in PROD
- 4. Reusible infra -> modules. we can use same code to create infra across different projects
- 5. Dependency management --> terraform can identify dependency between the resources 
- 6. CRUD --> Creating read update and delete the infra
- 7. inventory management -> we can read the terraform resources and understand what we are using
- 8. code and configuration (changes for every environment)
- Ansible --> Modules/collection/task
- terraform --> providers
- provider is like a plugin that lets terraform to interact with any platform API.
- before writing terraform code we need to write provider
- HCL  -> Hashicorp configuration language
- everything is in braces
<type of block> {
    key = "valie"
}

## Ansible is for configuration manaement. ansible is not grate to update and delete the infra
# IaaC -> Tools like terraform follows declarative way of creating infra
- 1. Version control infra
- 2. Reusable code called modules
- 3. CRUD
- 4. Inventory Management
- 5. cost effective
- 6. Dependency management
- 7. Consistent infra
- providers -> A Plugin that let terraform to connect with platform API to CRUD the resources
- Everything is block in terraform
    - resource
    - variable
    - terraform
    - provider
    - output
    - data etc.,
- resource "type of resource" "name you give{
    key = "value"
}

## terraform commands
 - **terraform init**       -> download provider file in to .terraform folder
 - **terraform plan**       -> reads the terraform file and gives us what is going to do
 - **terraform apply**      -> applys the infra
 - **terraform destroy**    -> delete the infra 

 - **terraform apply -auto-approve** --> applys the infra without asking prompt
 - **terraform destroy -auto-approve** --> delete the infra without asking prompt

 ## Variable syntax
 - variable "variable_name" {
    type : string/number/map/boolean/list
    default: "default_value"    
 }
