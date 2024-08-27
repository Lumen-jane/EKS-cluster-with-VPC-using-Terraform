# EKS-cluster-with-VPC-using-Terraform
Creation of AWS EKS cluster with VPC using Terraform

when i run terraform apply, I encountered this error:

 Error: waiting for EKS Node Group (maryjane-YIlhm6SAJI:node_group-20240827125129767500000012) create: unexpected state 'CREATE_FAILED', wanted target 'ACTIVE'. last error: eks-node_group-20240827125129767500000012-6ac8c9f2-166a-bbae-5607-51275ff374f6: AsgInstanceLaunchFailures: You've reached your quota for maximum Fleet Requests for this account. Launching EC2 instance failed.
│ 
│   with module.eks.module.eks_managed_node_group["node_group"].aws_eks_node_group.this[0],
│   on .terraform/modules/eks/modules/eks-managed-node-group/main.tf line 383, in resource "aws_eks_node_group" "this":
│  383: resource "aws_eks_node_group" "this" {
│ 

I guess it has to do with my account reaching the quota limit for Fleet Requests.
