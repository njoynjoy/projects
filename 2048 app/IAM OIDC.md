#To Assocaite IAM & EKS thriugh OIDC
```
eksctl utils associate-iam-oidc-provider --cluster $cluster_name --approve
```
```
curl -O https://raw.githubusercontent.com/kubernetes-sigs/aws-load-balancer-controller/v2.11.0/docs/install/iam_policy.json
```
