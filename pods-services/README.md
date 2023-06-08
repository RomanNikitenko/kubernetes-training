
# Pods
Create a pod from a yaml file:
```
$ kubectl apply -f pod-web-nodejs-next.yaml
```

Create a pod from an image:
```
$ kubectl run --image=quay.io/rnikitenko/web-nodejs-sample:next web
```

Get pods:
```
$ kubectl get pods
```

Delete a pod:
```
$ kubectl delete pod <podName>
```

Get logs for a pod:
```
$ kubectl logs <podName>
```

Get logs by selector(`latest-next` - is a selector name):
```
$ kubectl logs -l app=<latest-next>
```

Go to a container of a pod(`web-nodejs-next` - pod name, contains a one container, use `kubectl exec -it <POD_NAME> -c <CONTAINER_NAME> -- /bin/bash` if there are few containers ):
```
$ kubectl exec web-nodejs-next -ti -- /bin/sh
```

# Services
Run a service:
```
$ kubectl apply -f external-scoped-service.yaml
```

Get services:
```
$ kubectl get services
```

Delete a service:
```
$ kubectl delete service <serviceName>
```

# Base commands
Run all yaml files in the current directory:
```
$ kubectl apply -f .
```

Apply changes in the yaml file(pod or service is already running):
```
$ pod-web-nodejs-next.yaml
```

Kubectl explain (pod, for example):
```
$ kubectl explain pod 
```

Kubectl explain (a field of pod, for example):
```
$ kubectl explain pod.spec.restartPolicy 
```

Watch a command (get pods, for example):
```
$ watch kubectl get pods 
```

Diff:
```
$ kubectl diff -f pod-web-nodejs-next.yaml
```

API resources:
```
$ kubectl api-resources  
$ kubectl api-resources | grep apps 
```

Get nodes:
```
$ kubectl get nodes 
```

