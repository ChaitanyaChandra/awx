### KUBERNETES

* microk8s
```sh
sudo snap install microk8s --classic
sudo microk8s enable metallb
```
* minikube
```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64
```
### kustomize 
```sh
wget https://github.com/kubernetes-sigs/kustomize/releases/download/kustomize%2Fv5.4.3/kustomize_v5.4.3_linux_amd64.tar.gz
tar -zxvf kustomize_v5.4.3_linux_amd64.tar.gz
sudo mv kustomize /usr/local/bin/
kustomize version
```


### AWX INSTALL

* install
```sh
kustomize build . | kubectl apply -f -
```

* port forward
```
kubectl -n awx port-forward --address 0.0.0.0 service/awx-app-service 80
```

* retrieve secret
```
awx_secret=$(kubectl get secret awx-app-admin-password -o jsonpath=”{.data.password}” -n awx)
echo $awx_secret | tr -d '“”' | base64 -d
```
