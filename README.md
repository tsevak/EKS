## EKS CLUSTER

### Useful command to verify Instance type availibility per zones
```console
aws ec2 describe-instance-type-offerings --location-type availability-zone  --filters Name=instance-type,Values=t2.micro --region ap-southeast-2 --output table
```


###Create Cluster

```console
eksctl create cluster -f cluster.yaml -p iasadmin-ga
```
#### Verify Cluster

```console
k get nodes
```

#### Let create simple pod to verify
```console
 k run nginx --image=nginx
 k get pods
 ```