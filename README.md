# 🔑 Keycloak Cluster Service

Serviço de autenticação Keycloak em cluster com Nginx load balancer, integrado com banco de dados PostgreSQL, conteinerizado e orquestrado com Docker.


## ✔️ Objetivo e Funcionalidade

Prover soluções de autenticação e gerenciamento de usuários para endpoints por meio de um serviço arquitetado em cluster. A requisição é recebida pelo Nginx, que atua como load balancer, direcionando para alguma das duas instâncias do Keycloak, ambas integradas a um mesmo banco de dados PostgreSQL.


## 🚀 Tecnologias Utilizadas

* Docker
* Keycloak
* Nginx
* PostgreSQL

## ⚠️ Dependências

**[Docker](https://www.docker.com/)**


## 🐳 Endpoint (Opcional)

O repositório abaixo provê uma aplicação front-end simples em ReactJS integrada com o Keycloak para fins de teste do Keycloak Cluster Service. 

**[Keycloak React App](https://github.com/passosleo/keycloak-react-app)**



<!-- ## 🐳 Instalação

1️⃣ - Rode o comando abaixo:
```
docker run -d -p 3000:3000 --name keycloak-react-app leopassos/keycloak-react-app:1.0
```

2️⃣ - Acesse no navegador:
```
http://localhost:3000/
``` -->
