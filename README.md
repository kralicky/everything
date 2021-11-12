# everything

A helm chart to install (most of) the Bitnami helm charts. A few have been 
omitted due to redundancy/conflicts/needing a specific environment/etc.

Installation:
1. Install a default storage class of your choice

2. Install the helm controller manifests
```
kubectl create -f helm-controller/
```
3. Install everything
```
helm install everything chart/
```

See `image-list.txt` for an (almost) complete list of images which can be preloaded onto nodes.