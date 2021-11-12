# everything

A helm chart to install (most of) the Bitnami helm charts. A few have been 
omitted due to redundancy/conflicts/needing a specific environment/etc.

For testing purposes only! Don't install this on your production cluster. 

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
The total size of all images is ~16.4GB if exported into a single archive.

Total resource requests:
- Storage: 796GB
- Pods: 234
- Memory: 77.6Gi (actual usage is higher)
- VCPU: 26.83