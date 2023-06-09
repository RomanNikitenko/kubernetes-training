
# Deployment

- `replicas` - number of pods that is created using `template`
- `selector` - should match a pod for creation
- `matchLabels` - see value in the `template`

Create a deployment from a yaml file:
```
$ kubectl apply -f web-nodejs-next-deployment.yaml
```

Get deployments:
```
$ kubectl get deployment
```
# Krew
Package manager, helps to install kubectl plugins

Install tree:
```
$ kubectl krew install tree 
```

Display deployment using tree
```
$ kubectl tree deployment web-next-deployment
```

