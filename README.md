# k8s-wordpress
Roll out Wordpress with MySQL DB and NFS type PVC in k8s orchestration

## create secret
```yaml
kubectl create secret generic mysql-pass --from-literal='password=countonme'
```

## roll out all the yaml files in current dir
```yaml
cd k8s-wordpress
kubectl apply -f ./
```

## check if the wordpress is up and running
```shell
curl $NODE_IP:$NODE_PORT:31080/wp-admin/install.php?step=1
```

More details please check http://www.showerlee.com/archives/2336
