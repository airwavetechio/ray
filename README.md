# ray

This repo quickly show cases how to test RAY on a GKE cluster with AutoPilot, and the Ray Operator enabled. 


## Commands
## Getting setup
```
kubectl apply -f .
```
* Port forwarding for the dashboard: `kubectl port-forward svc/raycluster-autoscaler-head-svc 8265:8265 10001:10001`
* Kubectl exec in to the head pod: `kubectl exec -it <raycluster-headpod-name> -- /bin/bash`
* Within the pod - check file system: `df -h`
* Within the pod - run job: `cd /home/ray/samples && python test_4_gpu.py`
