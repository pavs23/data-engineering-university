# data-engineering-university
A place to learn data engineering


## Terraform 
Terraform is an infrastructure as code tool built by Hashicorp.

You can define databases, virtual machines, storage, security policies and more all using code.


### Learning Resources
* [Why we need terraform](https://www.youtube.com/watch?v=mzgfHmDRamk) or something like it (Video)
* [What is terraform cloud](https://developer.hashicorp.com/terraform/cloud-docs?utm_source=google&utm_channel_bucket=paid&utm_medium=sem&utm_campaign=Cloud_|_APJ_|_ANZ_|_ENG_|_GG_|_Search_|_Adopt_|_All_|_Terraform_|_Cloud_|_Brand&utm_content=19593308585-151005249008-645628325647&utm_offer=signup&gclid=Cj0KCQiA3eGfBhCeARIsACpJNU8TrDByPC6-XtAawW5IdxoNZ9AFPkS-KF7iVomEuxhLaxxCmZtnXiAaArT8EALw_wcB)
* [Terraform on AWS example](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/aws-build)



### Most common commands

```hcl

# initialises the terraform providers (these are like libraries)
terraform init


# cleans up the formatting of your code
terraform fmt


# validates what you've written locally
terraform validate


# compares your code to the remote terraform state (what has been deployed) and gives you diff, much like a git diff
terraform plan


# applies the changes from your plan
terraform apply
```

### Best Practice Recommendations

#### Managing your Terraform Workspace
* Terraform requires a place to store it's state file, the state file keeps track of all the deployed artifacts
  * you can do this yourself on some sort of object store such as S3
* I recommend you get terraform cloud to manage the state
  * It has other features like secret management and drift detection
* You can get terraform cloud to sync up with other CI tools like Github Actions, Buildkite and CircleCI to name a few


#### Terraform modules
* Using terraform modules is like writing your own library
* If you're creating the same two or more resources together, it would be cleaner to turn them into a module you can reuse




