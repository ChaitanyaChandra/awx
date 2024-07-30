### KUBERNETES

```sh
sudo snap install microk8s --classic
sudo microk8s enable metallb
```

### kustomize 
```sh
wget https://github.com/kubernetes-sigs/kustomize/releases/download/kustomize%2Fv5.4.3/kustomize_v5.4.3_linux_amd64.tar.gz
tar -zxvf kustomize_v5.4.3_linux_amd64.tar.gz
```


### AWX INSTALL

```sh
kustomize build . | kubectl apply -f -
```


