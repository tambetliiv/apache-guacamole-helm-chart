# Apache guacamole

A helm chart for apache guacamole. 

This helm chart provides a complete setup of:

- Guacamole server
- Guacd Proxy
- MySQL server

Prerequisites:

- Kubernetes v1.17
- Helm v3.0.3

You can get it up ang running by:

1. `git clone` this repo
1. `cd apache-guacamole-helm-chart`
1. `kubectl create namespace guacamole`
1. `helm install guacamole . --namespace=guacamole -f values.yaml`
  - (optional) admin password and ssh host connection can be set using: `--set global.adminPassword=admin,guacamole.ssh.host=host,guacamole.ssh.user=username,guacamole.ssh.password=pass`
1. `kubectl --namespace guacamole port-forward svc/guacamole 8080:80`
1. visit http://localhost:8080/guacamole in your browser. Default creds are admin/admin 

