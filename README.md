# Projeto rotten-potatoes

### Objetivo
O projeto rotten-potatoes é uma aplicação escrita em Python e tem como objetivo ser uma aplicação de exemplo pra trabalhar com o uso de containers.

### Configuração
Pra configurar a aplicação, é preciso ter um banco de dados Mongo e pra definir o acesso ao banco, configure as variáveis de ambiente abaixo:

MONGODB_DB => Nome do database

MONGODB_HOST => Host do MongoDB

MONGODB_PORT => Posta de acesso ao MongoDB

MONGODB_USERNAME => Usuário do MongoDB

MONGODB_PASSWORD => Senha do MongoDB

### Execução com kubernetes K3D

```bash
k3d cluster create meu-cluster \
-p "5000:30000@loadbalancer"
```

```bash
# pwd src
docker build -t jefersonalmeida/rotten-potatoes:v1 .
```

```bash
# pwd src
docker push jefersonalmeida/rotten-potatoes:v1
```

```bash
# pwd src
kubectl apply -f deployment.yaml
```
