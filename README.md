# 🔑 Keycloak Cluster Service

Serviço de autenticação Keycloak em cluster com Nginx load balancer, integrado com banco de dados PostgreSQL, conteinerizado e orquestrado com Docker.


## ✔️ Objetivo e Funcionalidade

Prover soluções de autenticação e gerenciamento de usuários para endpoints por meio de um serviço arquitetado em cluster. A requisição é recebida pelo Nginx, que atua como load balancer, direcionando para alguma das duas instâncias do Keycloak, ambas integradas a um mesmo banco de dados PostgreSQL. O serviço roda de forma conteinerizada orquestrada pelo Docker.

## 🔁 Fluxograma

<img  width="640" src="https://user-images.githubusercontent.com/90735184/158608991-10152f05-e6af-4f9e-b3d8-7e485b406908.png">


## 🚀 Tecnologias Utilizadas

* Docker
* Keycloak
* Nginx
* PostgreSQL

## ⚠️ Dependências

Este serviço requer o **[Docker](https://www.docker.com/)** para ser executado.


## 🖥️ Endpoint (Opcional)

O repositório abaixo provê uma aplicação front-end simples em ReactJS integrada com o Keycloak para fins de teste do Keycloak Cluster Service. 

**[Keycloak React App](https://github.com/passosleo/keycloak-react-app)**



## 🐳 Instalação

Baixe o repositório em um local de sua preferência:
```
git clone https://github.com/passosleo/keycloak-cluster-service.git
```

Acesse a pasta do projeto:
```
cd keycloak-cluster-service
```

Rode o comando abaixo:
```
docker compose up -f docker-compose.yml
```

Acesse o painel administrativo do Keycloak em:
```
http://localhost:8000/
```
