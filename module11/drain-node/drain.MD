### evict all pods from a node
```
kubectl drain cadmin
```
### make a node scheduable again
```
kubectl cordon
kubectl uncordon
```

```
curl -v -H 'Content-type: application/json' --key client.key --cert client.crt https://192.168.34.2:6443/api/v1/namespaces/default/pods/nginx-deployment-6799fc88d8-ds499/eviction -d @eviction.json

{
  "apiVersion": "policy/v1",
  "kind": "Eviction",
  "metadata": {
    "name": "nginx-deployment-6799fc88d8-ds499",
    "namespace": "default"
  }
}
```