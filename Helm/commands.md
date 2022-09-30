### List, Add, remove Repo 

```console
helm repo list
helm repo add bitnami https://charts.bitnami.com/bitnami
helm repo update
helm repo list
helm repo remove bitnami
```


### Search the repository
```console
helm search repo mysql
helm search repo apache --versions
helm search repo bitnami < REP-NAME >
helm search repo bitnami/apache --versions
```

### Install a Package

```console
helm install webserver bitnami/apache
```
### To check the installation status:
```console
helm status webserver
```

### To Upgrade:
```console
ROOT_PASSWORD=$(kubectl get secret --namespace default mydb-mysql -o jsonpath="{.data.mysql-root-password}" | base64 --decode)
helm upgrade mysql-release bitnami/mysql --set auth.rootPassword=$ROOT_PASSWORD
```

### To uninstall installed Pkg
```console
helm uninstall webserver
```