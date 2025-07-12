#Create a fargate profile
```
eksctl create fargateprofile \
    --cluster <your-cluster-name> \
    --region us-east-1 \
    --name alb-sample-app \
    --namespace game-2048
```
#Link for 2048 game 
Deploy in cluster u have created

```
kubectl apply -f https://raw.githubusercontent.com/kubernetes-sigs/aws-load-balancer-controller/v2.5.4/docs/examples/2048/2048_full.yaml
```
