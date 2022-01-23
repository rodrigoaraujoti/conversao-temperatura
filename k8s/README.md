# Instruções para execução no Kubernetes K3D

## _Excluindo cluster antigo_
```sh
k3d cluster delete meucluster
```
```sh
k3d cluster list
```
```sh
docker container ls
```

## _Criando cluster_
Rodando na porta 8081
```sh
k3d cluster create meucluster --servers 1 --agents 2 -p "8081:30000@loadbalancer"
```
```sh
kubectl apply -f deployment.yaml
```

## _Push em docker hub_
```sh
docker login
```
```sh
docker build -t rodrigoaraujoti/conversao-temperatura:v1 .
```
```sh
docker tag rodrigoaraujoti/rotted-potatoes:v1 rodrigoaraujoti/conversao-temperatura:latest
```
```sh
$ docker push rodrigoaraujoti/conversao-temperatura:v1
```
