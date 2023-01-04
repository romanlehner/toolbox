# Kubernetes
## kubectl
### Context
Configure multiple cluster contexts

    export KUBECONFIG=$KUBECONFIG:~/.kube/cluster_a:~/.kube/cluster_b

Merge contexts to `~/.kube/config`:

    kubectl config view --flatten > ~/.kube/config

### JSON Path
Get pod name by label and re-use it in other commands

    kubectl get logs "${kubectl get pod -l app=app -o jsonpath='{.items[0].metadata.name}'}"
    
## Pods
### Run container indefinetaly
```yaml
spec:
  containers:
    - command: ['/bin/sh', '-c', '--']
      args: ['while true; do sleep 30; done;']
      name: ...
      image: ...
```
