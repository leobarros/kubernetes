# Estudos sobre Istio

Obs: usando um cluster separado usando o k3d

Criei um cluster com o nome de istio-estudos com:
`k3d cluster create istio-estudos --servers 3`

## Versão do istio

Versão 1.13.0

## Instalando o istio em sua máquina

```bash
curl -L https://istio.io/downloadIstio | ISTIO_VERSION=1.13.0 TARGET_ARCH=x86_64 sh -
```

Mova o binário para /usr/local/bin com `sudo cp istio-1.13.0/bin/istioctl /usr/local/bin`

## Fazendo uma demonstração

Colocando um namespace para o istio visualizar
`kubectl label namespace lsales istio-injection=enable`

Instalando a demo

```bash
istioctl install --set profile=demo -y
✔ Istio core installed
✔ Istiod installed
✔ Egress gateways installed
✔ Ingress gateways installed
✔ Installation complete
Making this installation the default for injection and validation.
```