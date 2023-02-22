---
sidebar_position: 1
---

# What is Infrastructure as Code with Terraform?

Infrastructure as code (IaC) tools allow you to manage infrastructure with configuration files rather than through a graphical user interface. IaC allows you to build, change, and manage your infrastructure in a safe, consistent, and repeatable way by defining resource configurations that you can version, reuse, and share.

Terraform is HashiCorp's infrastructure as code tool. It lets you define resources and infrastructure in human-readable, declarative configuration files, and manages your infrastructure's lifecycle. Using Terraform has several advantages over manually managing your infrastructure:

- Terraform can manage infrastructure on multiple cloud platforms.
- The human-readable configuration language helps you write infrastructure code quickly.
- Terraform's state allows you to track resource changes throughout your deployments.
- You can commit your configurations to version control to safely collaborate on infrastructure.

## Standardize your deployment workflow

![Alt text](https://learn.hashicorp.com/img/terraform/terraform-iac.png)

## Build Infrastructure

### Prerequisites

To follow this tutorial you will need:

- The [Terraform CLI](https://learn.hashicorp.com/tutorials/terraform/install-cli) (0.14.9+) installed.
- The [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html) installed.
- [An AWS account](https://aws.amazon.com/free/).
- Your AWS credentials. You can [create a new Access Key on this page](https://console.aws.amazon.com/iam/home?#/security_credentials).

### Usage

- Specify the AWS region to create resources into, using region variable.

- Specify the aws-cli profile for the account to create resources in, using profile variable.
    The default location to view your aws-cli profiles is $HOME/.aws/credentials on Linux and macOS and %USERPROFILE%\.aws\credentials on Windows.
    There are a number of other options for authenticating with the AWS Provider. These can be found here: [https://registry.terraform.io/providers/hashicorp/aws/latest/docs](https://registry.terraform.io/providers/hashicorp/aws/latest/docs). To implement other strategies, replace the profile property of the aws provider as appropriate.

### Initialize the directory

```md
terraform init
```

### Format and validate the configuration

```md
terraform validate
```

### Create execution plan

```md
terraform plan
```

### Create infrastructure

```md
terraform apply
```

### Inspect state

```md
terraform show
```

### Terraform Target (run terraform only for a specific resource)

```md
terraform state list
terraform apply -target aws_ecs_service.admin
```
