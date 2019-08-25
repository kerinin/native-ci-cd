# K8s native CI/CD

## Currents Status

Tekton seems pretty nice. The UI is good and the design makes sense. Install is
pretty easy. Would like to use.

Prow doesn't feel ready for prime time. The UI is useless for debugging initial
configuration issues, testing it is a PITA, it appears to assume that the
repositories you're watching belong to an organization, and timers don't seem to
fire in some cases (possibly only fire if the previous trigger completed?).

At this point it's probably best to use something better packaged (JenkinsX or
Circle or something).


## Usage

```
# Install the Tekton CRD and operators
kubctl apply -k base/tekton

# Some sample pipelines
kubectl apply -k base/pipelines

# Find the assigned node-port - you should be able to 
# open localhost:##### and see the Tekton dashboard
kubectl get svc --namespace tekton-pipelines

# Install prow
kubectl apply -k base/prow
```
