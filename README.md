# Exercício: Gerenciando Aplicações com kubectl e Minikube

## Descrição

O exercício consiste na criação e no gerenciamento de uma aplicação Nginx em um cluster Kubernetes local, utilizando Minikube e kubectl. 

## Pré-requisitos

- Minikube instalado e rodando  
- kubectl instalado e rodando 
- Git instalado para versionamento e entrega  

## Instruções de Uso

1. Aplicar o Deployment:  
 
   kubectl apply -f nginx-deployment.yaml
Aplicar o Service:
kubectl apply -f nginx-service.yaml

Verificar os pods
kubectl get pods

Acessar a aplicação
minikube service nginx-service --url

Para escalar a aplicação, editar o arquivo nginx-deployment.yaml alterando replicas e aplicar novamente
kubectl apply -f nginx-deployment.yaml

Para limpar o ambiente
kubectl delete -f nginx-service.yaml
kubectl delete -f nginx-deployment.yaml

### Página Nginx no navegador  

![Página Nginx](imagens/print.png)

### Pods em execução (5 réplicas)  

![Pods 5 réplicas](imagens/print2.png)
