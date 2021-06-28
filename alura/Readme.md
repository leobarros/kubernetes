# Kubernetes - Alura

Vamos colocar um portal de notícias no K8s.

## Executando o exemplo

`kubectl apply -f exemplo`

Teremos a seguinte saída:

```bash
pod/pod-1 created
pod/pod-2 created
pod/primeiro-pod-declarativo created
pod/segundo-pod-declarativo created
service/svc-pod-1-loadbalancer created
service/svc-pod-1 created
service/svc-pod-2 created
```

Verificando o status dos recursos

`kubectl get pods -o wide`
`kubecetl get svc`

Para acessar a aplicação de exemplo. Uma página do Nginx padrão. É necessário saber o ip do seu node:

Faça o comando `kubectl get nodes -o wide` em seu terminal e pegue o ip que fica em *INTERNAL-IP:30000* para acessar diretamente o serviço *NodePort* ou se preferir *INTERNAL-IP:31000* para acessar por meio do serviço *Load Balancer*
