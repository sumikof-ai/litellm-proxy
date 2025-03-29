

kubectl create configmap litellm-config-file --from-file=config.yaml --save-config --dry-run=client -o yaml | kubectl apply -f -

kubectl create secret generic litellm-secrets --from-literal=OPENAI_API_KEY=<OPENAI_API_KEY>

kubectl apply -f kubernetes/deployment.yaml
kubectl apply -f kubernetes/service.yaml