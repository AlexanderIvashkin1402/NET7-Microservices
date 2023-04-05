Order of K8S deployemnts
----------------------------------------
1.  Update C:\Windows\System32\drivers\etc\hosts - add line 127.0.0.1 acme.com
2.  kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.7.0/deploy/static/provider/aws/deploy.yaml
3.  kubectl apply -f ingress-srv.yaml
4.  kubectl apply -f local-pvc.yaml
5.  kubectl create secret generic mssql --from-literal=SA_PASSWORD="pa55w0rd!"
6.  kubectl apply -f mssql-plat-depl.yaml
7.  kubectl apply -f rabbitmq-depl.yaml
8.  kubectl apply -f platforms-depl.yaml
9.  [optional - development only] kubectl apply -f platforms-np-srv.yaml
10. kubectl apply -f commands-depl.yaml
