# velero-scripts


Check the official documentation at: 

https://github.com/vmware-tanzu/velero
https://github.com/vmware-tanzu/velero-plugin-for-microsoft-azure

### Snippets
```
kubectl create namespace demo
kubectl create deployment nginx --image=nginx -n demo   
kubectl expose deploy/nginx --port 80 -n demo

velero backup create backup --include-namespaces demo

velero backup get

velero restore create --from-backup backup --namespace-mappings demo:restore


kubectl logs deployment/velero -n velero
```