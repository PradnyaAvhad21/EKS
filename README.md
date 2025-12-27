**2.1 Creating AWS Account & IAM Users**

Create an AWS account and verify billing details

Log in to AWS Management Console

Enable MFA for root account (recommended)

Create IAM users instead of using root

Assign permissions using IAM groups or policies

Generate Access Key & Secret Key for programmatic access

**2.2 Configuring AWS CLI & kubectl**

Install AWS CLI on local machine

Configure CLI using aws configure

Set default region and output format

Install kubectl for Kubernetes management

Update kubeconfig using

aws eks update-kubeconfig --name

Verify access using

kubectl get nodes

**2.3 Preparing Networking for EKS**

Create a VPC with appropriate CIDR

Create public and private subnets across AZs

Associate subnets with correct route tables

**Security Groups Configuration**

Create Security Group in the VPC

Define inbound rules (SSH, node communication, etc.)

Define outbound rules (generally allow all)

Attach Security Group to EKS worker nodes

**Internet Gateway (IGW) Setup**

Create and attach Internet Gateway to VPC

Update route tables with 0.0.0.0/0 → IGW

Enables worker nodes to pull images & access internet

**IAM Policies for EKS**

Create custom IAM policies (EC2, EKS, ECR, ELB)

Attach policies to IAM roles

Assign IAM role to EKS worker nodes

Ensures secure AWS service access
