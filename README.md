# squid

kubectl port-forward svc/argocd-server -n argocd 8080:443  
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo  
docker kill --signal=SIGHUP squid_container_id  