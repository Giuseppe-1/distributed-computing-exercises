kubectl apply -f database-deployment.yml
kubectl apply -f database-service.yml
kubectl apply -f webapp-deployment.yml
kubectl apply -f webapp-service.yml

minikube service --url webapp

curl -v "$(minkube service --url webapp)/ping"
curl -v -X POST $(minikube service --url webapp) -d "full\_url=https://www.redhat.com"
curl -v $(minikube service --url webapp)/2pTO3J3 # Change the uuid with the one generated in the previous request

