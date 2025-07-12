Hi Thanks for visiting my repository. 
Today, we are going to create an EKS cluster. So, how will we create an EKS cluster? 
What is EKS? EKS is an AWS service. It means Elastic Kubernetes Service. 
--**install EKS through below link**
https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html#windows_kubectl
**--install AWS CLI through below link**
https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
**--install kubectl through below link**
https://docs.aws.amazon.com/eks/latest/userguide/install-awscli.html

Deployed 2048 game in AWS through EKS Cluster

EKS: EKS simplifies cluster management by providing a fully managed control plane.

AWS Fargate: A serverless compute engine for containers. In simple terms, using Fargate means no need to manage EC2 instances. It offers maximum abstraction and high availability.

Secure IAM Integration with OIDC: Allows Kubernetes service accounts to securely grant permissions to interact with AWS services. Here, we have used it to create a load balancer with the ALB controller.

In Ingress, we define routing rules for external access.

The Ingress Controller continuously watches for Ingress resources. When it finds them, it will automatically create and configure an Application Load Balancer (ALB) in the public subnet.

Procedure followed:

In my Windows laptop, installed MobaXterm. With the help of WSL, I was able to connect to Ubuntu.

Installed AWS CLI, eksctl, and kubectl.

Configured AWS to the Ubuntu with aws configure.

Created the cluster with eksctl create cluster --name <your cluster name> --region <your region name> --fargate.

Used IAM OIDC (OpenID Connect) provider as the identity provider for my created cluster -- IAMOIDC

Deployed the 2048 game YAML file through kubectl apply -f.

Created an IAM policy.

Created the IAM service account for the cluster and attached the policy to it.

Added the Helm repo of EKS.

Installed Application Load Balancer controller through Helm


Key takeaway: A real-world experience with EKS, Fargate, IAM, Helm, and Kubernetes networking — all while deploying something fun and visual with 2048 game

