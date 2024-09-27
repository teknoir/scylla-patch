# Temporary patch to allow Teknoir tunnels to the Scylla Dashboard

## Apply the patch
```bash
# Add the configmap
kubectl -n scylla apply -f https://raw.githubusercontent.com/teknoir/scylla-patch/main/configmap.yaml
# Patch the deployment
kubectl -n scylla patch deployment scylla-services --patch "$(curl -s https://raw.githubusercontent.com/teknoir/scylla-patch/main/patch.yaml)"
```

