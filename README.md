- [Getting Started](#Getting-started)
- [Setup your environment ](#Create_instrafracure) 
  
### Prerequisites
- Docker 20.10.0+
- Helm >= 3.0
- Kind 0.17.0+

## Getting Started
1. Create kubernetes cluster on docker environment by kind
```bash
$ kind create cluster --config kind-config.yaml
```
2. Set kubeconfig context to kind.
3. clone repo to your local machine 
```bash
$ git clone git@github.com:danielba23/rtg-helm.git
```
### Setup your environment

1. install helm chart  
```bash
$ helm install tirgol . -f values.yaml
```
2. establish connction to rtg
```bash
$ kubectl port-forward svc/tirgol-rtg-nginx 8899:80
```
3. connect to nginx via your browser - 
<img width="1432" alt="Screen Shot 2022-12-27 at 19 31 51" src="https://user-images.githubusercontent.com/62659741/209701497-07eae80c-6898-43e7-a1f2-a5f2217461b8.png">

