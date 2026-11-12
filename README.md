# AWS Cloud Infrastructure with Terraform

This project provisions a basic AWS networking environment using Terraform and Infrastructure as Code.

## Infrastructure Created

The Terraform configuration creates:

- A custom AWS VPC
- A public subnet
- An Internet Gateway
- A public route table
- A route table association
- A security group
- An outbound security group rule

## Architecture

The network follows this structure:

**VPC → Public Subnet → Route Table → Internet Gateway**

The public subnet is associated with the public route table, which routes internet-bound traffic through the Internet Gateway.

## AWS Region

The infrastructure is deployed in:

`eu-north-1` — Europe (Stockholm)

## Technologies

- AWS
- Terraform
- Git
- GitHub
- Command Line

## Terraform Workflow

The infrastructure was provisioned using the standard Terraform workflow:

```bash
terraform init
terraform validate
terraform plan
terraform apply
```

Terraform state was also checked using:

```bash
terraform state list
```

A final `terraform plan` confirmed that the deployed AWS infrastructure matches the Terraform configuration with no outstanding changes.

## Project Purpose

The purpose of this project is to demonstrate AWS infrastructure provisioning and networking automation using Terraform, including network segmentation, internet routing, and security controls.
