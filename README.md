

# **Module: Mastering Terraform**

---

##  **Introduction**

So far in this DevOps Dive Deep course, you've:

- Used **Git** for version control  
- Built and deployed apps using **Jenkins**  
- Containerized them using **Docker**  
- Orchestrated them using **Kubernetes** on **AWS EKS**  

But how did you provision that EC2?  
How was your VPC designed?  
How do you make your infrastructure **reproducible**, **scalable**, and **auditable**?

That’s where **Terraform** comes in.

Terraform is a **declarative, cloud-agnostic Infrastructure as Code (IaC)** tool that allows you to provision and manage cloud infrastructure **consistently and automatically** using version-controlled code.

In this module, you'll move from **manual AWS setups** to **real-world, automated, production-grade deployments** using Terraform — with **two complete projects** along the way.

---

#  Module Objective

To make you proficient in building, managing, and scaling cloud infrastructure on AWS using Terraform and best IaC + SRE practices.

---

#  Course Structure

---

## Section 1 – Infrastructure as Code (IaC) Fundamentals

- What is Infrastructure as Code  
- Benefits of IaC in DevOps and SRE  
- Declarative vs Imperative approaches  
- Tools comparison: Terraform vs CloudFormation vs Pulumi  
- GitOps and Infra versioning  
- Real-world IaC pipeline flow  

---

## Section 2 – Terraform Basics

- What is Terraform and why it's used  
- Architecture and workflow  
- Install Terraform on macOS, Linux, and Windows  
- CLI commands: `init`, `plan`, `apply`, `destroy`, `validate`  
- Anatomy of a Terraform configuration: providers, resources, variables  
- Lab:  
  - Install Terraform  
  - Write your first main.tf  
  - Deploy a simple AWS resource (S3 bucket or EC2)  

---

## Section 3 – Providers, Resources, and Terraform Settings

- What is a provider  
- AWS provider setup  
- Terraform backend configuration  
- `required_providers`, `required_version` blocks  
- Resource block structure  
- Lifecycle meta-arguments (create_before_destroy, prevent_destroy)  
- Lab: Provision EC2, S3, and VPC resources  

---

## Section 4 – Variables and Data Sources in Terraform

- Input variables and types  
- Output variables  
- Locals for reusable expressions  
- Data sources to reference existing AWS infrastructure  
- Sensitive variables and secrets  
- Lab:  
  - Pass variables via CLI, files, and environment  
  - Reference existing VPC ID or AMI using data sources  

---

## Section 5 – Terraform Meta-Arguments and Looping Constructs

- count and for_each  
- dynamic blocks  
- splat operators  
- conditional expressions  
- Lab:  
  - Deploy multiple EC2 instances  
  - Use looping to configure security group rules  
  - Dynamically generate tags or subnets  

---

## Section 6 – AWS VPC and 3-Tier Network Architecture

- What is a VPC  
- Subnets: public, private, isolated  
- Route tables and IGWs  
- NAT gateways and Bastion hosts  
- Security groups and NACLs  
- Lab:  
  - Build 3-tier architecture with Terraform  
  - Separate app, DB, and web layers  

---

## Section 7 – EC2 Instances and Security Groups

- Launch EC2 instances in VPC  
- Create and associate key pairs  
- Add user_data for bootstrapping  
- Configure security groups for web, SSH, DB  
- Lab: Deploy EC2-based web and DB tiers with secure SG rules  

---

## Section 8 – Load Balancing with Terraform

### Combined into one logical section covering all ALB use cases:

- Create Application Load Balancer (ALB)  
- Target groups and listener rules  
- Context-path based routing  
- Host-header based routing  
- Redirects using headers and query strings  
- Lab:  
  - Route traffic from ALB to multiple EC2 services  
  - Use host and path rules to simulate microservices  

---

## Section 9 – DNS and Route53 Integration

- AWS Route53 overview  
- Record types (A, CNAME, Alias)  
- Create custom DNS entries using Terraform  
- Map ALB to domain  
- Lab:  
  - Point domain to ALB using Route53  
  - Validate routing by accessing microservices with DNS  

---

## Section 10 – Autoscaling with Launch Configurations and Templates

- Autoscaling groups: basics and benefits  
- Launch configurations vs Launch templates  
- Use cases and trade-offs  
- Health checks and lifecycle hooks  
- Lab:  
  - Create ASG with launch template  
  - Attach ALB to ASG  
  - Set scaling policies and thresholds  

---

## Section 11 – Network Load Balancer (NLB) with TCP and TLS

- NLB vs ALB  
- Use case for TCP/UDP workloads  
- Configure TLS listener  
- Lab: Deploy a high-performance NLB for backend apps  

---

## Section 12 – Monitoring and Alerting with CloudWatch

- Create CloudWatch alarms using Terraform  
- Monitor ALB metrics, ASG CPU, and EC2 health  
- Action targets: SNS, autoscaling, shutdown  
- Lab:  
  - Configure 3 different CloudWatch alarms  
  - Trigger email or scaling policy  

---

## Section 13 – Terraform Modules – Reuse and Organize Code

- What are modules and why use them  
- Structure: inputs, outputs, main.tf  
- Create reusable modules  
- Reference modules locally and remotely  
- Lab:  
  - Build a VPC module  
  - Reuse it in multiple environments (dev, prod)  
  - Create module for ALB and EC2  

---

## Section 14 – Remote State and State Locking

- Terraform state explained  
- Problems with local state  
- Remote state backend using S3  
- State locking with DynamoDB  
- Lab:  
  - Store state in S3  
  - Lock and protect with DynamoDB  
  - Enable versioning and recovery  

---

## Section 15 – Final Project

**Project: Scalable, Modular Web Architecture with Observability**

- Build a complete 3-tier architecture using Terraform  
- Use custom modules for VPC, EC2, ALB, and ASG  
- Configure Route53, NLB, and DNS-based routing  
- Attach CloudWatch alarms and monitoring  
- Store state remotely with S3 and DynamoDB  
- Use ALB for microservices routing  
- Implement autoscaling for high availability  

---

