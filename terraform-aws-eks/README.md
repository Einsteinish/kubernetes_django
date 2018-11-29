# terraform-aws-eks

Deploy a full AWS EKS cluster with Terraform and Django App

1. VPC
2. Internet Gateway (IGW)
3. Public and Private Subnets
4. Security Groups, Route Tables and Route Table Associations
5. IAM roles, instance profiles and policies
6. An EKS Cluster
7. Autoscaling group and Launch Configuration
8. Worker Nodes in a private Subnet
9. The ConfigMap required to register Nodes with EKS
10. KUBECONFIG file to authenticate kubectl using the heptio authenticator aws binary
11. Deploying Django app via "kubectl apply -f deploy/*"

## Configuration

You can configure you config with the following input variables:

| Name                 | Description                       | Default       |
| -------------------- | --------------------------------- | ------------- |
| `cluster-name`       | The name of your EKS Cluster      | `my-cluster`  |
| `aws-region`         | The AWS Region to deploy EKS      | `us-west-2`   |
| `node-instance-type` | Worker Node EC2 instance type     | `m4.large`    |
| `desired-capacity`   | Autoscaling Desired node capacity | `2`           |
| `max-size`           | Autoscaling Maximum node capacity | `5`           |
| `min-size`           | Autoscaling Minimum node capacity | `1`           |
| `vpc-subnet-cidr`    | Subnet CIDR                       | `10.0.0.0/16` |

## Tutorials
[Docker & Kubernetes : Terraform and AWS EKS](https://www.bogotobogo.com/DevOps/Docker/Docker_Kubernetes_Terraform_EKS.php)
