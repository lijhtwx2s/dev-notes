# Kubernetes Cheatsheet

## Common kubectl commands

- `kubectl get pods -A` - list all pods in all namespaces
- `kubectl logs <pod> -f` - follow logs
- `kubectl exec -it <pod> -- /bin/sh` - shell into pod
- `kubectl port-forward svc/<svc> 8080:80` - forward service port

## Quick YAML snippet

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: debug
spec:
  containers:
  - name: debug
    image: busybox
    command: ["sleep", "3600"]
```