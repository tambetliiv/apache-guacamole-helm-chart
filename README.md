# Apache guacamole

A helm chart for apache guacamole. 

This helm chart provides a complete setup of:

- Guacamole server
- Guacd Proxy
- MySQL server

You can get it up ang running by:

1. git clone this repo
1. cd apache-guacamole-helm-chart
1. helm repo add mysql https://kubernetes-charts.storage.googleapis.com/
1. helm dependency update
1. kubectl create namespace guacamole
1. helm install guacamole . --namespace=guacamole -f values.yaml
1. kubectl --namespace guacamole port-forward svc/guacamole 8080:80
1. visit http://localhost:8080/guacamole in your browser. Default creds are guacadmin/guacadmin

