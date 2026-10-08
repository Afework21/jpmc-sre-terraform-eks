# JPMC SRE Lab — Terraform AWS EKS

A hands-on Site Reliability Engineering project demonstrating how to provision AWS infrastructure and an Amazon EKS Kubernetes cluster using Terraform and reusable infrastructure modules.

## Project Overview

This repository contains the Infrastructure-as-Code portion of my SRE lab.

The goal is to demonstrate practical experience with:

- Terraform
- AWS
- Amazon EKS
- Amazon VPC
- Kubernetes
- Infrastructure as Code (IaC)
- Modular infrastructure design
- Production-oriented SRE practices

## Architecture

```text
AWS
│
├── VPC
│   ├── Public Subnets
│   └── Private Subnets
│
└── Amazon EKS
    ├── Kubernetes Control Plane
    └── Worker Nodes
```

Terraform is used to provision and manage the AWS infrastructure in a repeatable and version-controlled manner.

## Repository Structure

```text
terraform/
├── main.tf
├── variables.tf
├── outputs.tf
├── .terraform.lock.hcl
└── modules/
    ├── vpc/
    │   ├── main.tf
    │   └── outputs.tf
    └── eks/
        ├── main.tf
        └── variables.tf
```

## Deployment Workflow

Initialize Terraform:

```bash
terraform init
```

Review the infrastructure changes:

```bash
terraform plan
```

Deploy the infrastructure:

```bash
terraform apply
```

Validate the configuration:

```bash
terraform validate
```

Destroy lab infrastructure when it is no longer required:

```bash
terraform destroy
```

## SRE Practices Demonstrated

This project demonstrates:

- Infrastructure automation
- Repeatable cloud deployments
- Terraform module design
- Kubernetes infrastructure provisioning
- AWS networking
- Infrastructure validation
- Git-based infrastructure management
- Environment cleanup and cost awareness

## Security

Sensitive Terraform artifacts are excluded from source control.

The repository does not commit:

```text
.terraform/
*.tfstate
*.tfstate.*
*.tfvars
.env
*.pem
*.key
```

AWS credentials and other secrets should be managed outside the repository.

## Reliability Goals

Example SRE targets used throughout the broader lab:

| SLI | Target |
|---|---:|
| Availability | 99.9% |
| P99 latency | < 300 ms |
| Error rate | < 0.1% |

These targets provide a basis for monitoring, alerting, and reliability engineering exercises.

## Related Lab Components

This Terraform project is part of a larger SRE portfolio that also covers:

- CI/CD pipelines
- Docker containerization
- Kubernetes application deployment
- Prometheus and Grafana
- Dynatrace
- OpenTelemetry
- Distributed tracing
- Incident troubleshooting
- Chaos engineering

## Skills Demonstrated

**Terraform · AWS · Amazon EKS · Kubernetes · Infrastructure as Code · VPC · SRE · DevOps**