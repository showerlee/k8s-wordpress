# k8s-wordpress
Roll out Wordpress with MySQL DB and NFS type PVC in k8s orchestration

### Create secret object via CLI
```yaml
kubectl create secret generic mysql-pass --from-literal='password=countonme'
```

### One-time roll out all yaml files in current dir
```yaml
cd k8s-wordpress
kubectl apply -f ./
```

### Check if the wordpress is up and running
```shell
curl $NODE_IP:31080/wp-admin/install.php?step=1
```

More details please check http://www.showerlee.com/archives/2336
