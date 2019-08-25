# K8s native CI/CD

keeping track of what I find

```
# Install the Tekton CRD and operators
kubctl apply -k base/tekton

# Some sample pipelines
kubectl apply -k base/pipelines

# Find the assigned node-port - you should be able to 
# open localhost:##### and see the Tekton dashboard
kubectl get svc --namespace tekton-pipelines
```
