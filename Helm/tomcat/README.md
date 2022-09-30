### Install tomcat 10.4.0 via Helm 
```console
helm install tomcat bitnami/tomcat --version 10.4.0 --values values.yaml
```

### Upgrade tomcat to latest version with preserving custom values which passed while first installation
```console
helm upgrade tomcat bitnami/tomcat --values values.yaml --dry-run   ### Dry-run to verify 
helm upgrade tomcat bitnami/tomcat --values values.yaml
```
### Verify
```console
k get pods
k get svc
minikube service tomcat
```
