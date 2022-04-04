# 🔑 Keycloak Cluster Service

Serviço de autenticação Keycloak em cluster com NGINX load balancer, integrado com banco de dados PostgreSQL, conteinerizado e orquestrado com Docker.


## ✔️ Objetivo e Funcionalidade

Prover soluções de autenticação e gerenciamento de usuários para endpoints por meio de um serviço arquitetado em cluster. A requisição é recebida pelo NGINX, que atua como load balancer, direcionando para alguma das duas instâncias do Keycloak, ambas integradas a um mesmo banco de dados PostgreSQL. O serviço roda de forma conteinerizada orquestrada pelo Docker.

## 🔁 Fluxograma

<img  width="640" src="https://user-images.githubusercontent.com/90735184/158608991-10152f05-e6af-4f9e-b3d8-7e485b406908.png">


## 🚀 Tecnologias Utilizadas

* Docker
* Keycloak
* NGINX
* PostgreSQL

## ⚠️ Dependências

Este serviço requer o **[Docker](https://www.docker.com/)** para ser executado.


## 🖥️ Endpoint (Opcional)

O repositório abaixo provê uma aplicação front-end simples em ReactJS integrada com o Keycloak para fins de teste do Keycloak Cluster Service. 

👉🏻 **[Keycloak React App](https://github.com/passosleo/keycloak-react-app)**

Siga o guia abaixo para configuração:

👉🏻 **[Guia de integração e configuração](https://jamboard.google.com/d/1p2sjMIA_BHvASBq7ffZ7mO2NGqeFy48nwczDjBWZuSU/viewer)**


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
docker compose -f docker-compose.yml up
```

Acesse o painel administrativo do Keycloak em:
```
http://localhost:8000/
```


## ❓ Como testar

Após compor o serviço no docker, rode o comando abaixo:
```
docker ps
```

Se tudo ocorreu bem, você verá quatro containers:

![image](https://user-images.githubusercontent.com/90735184/158616056-bd4da1ca-c1bf-4f28-b0b6-85eeb98a1ceb.png)

Acesse o painel administrativo do Keycloak em:
```
http://localhost:8000/
```

Encerre alguma das instâncias do keycloak:
```
docker kill kc1 
ou
docker kill kc2
```

Ao encerrar qualquer uma das instâncias, o painel administrativo deve permanecer acessível e com a sessão ativa. Caso esteja integrado ao front-end, os usuários devem permanecer aptos a realizar login ou com suas respectivas sessões ativas.

Para retomar a execução do Keycloak:
```
docker start kc1
ou
docker start kc2
```

As portas de acesso do Keycloak e do PostgreSQL podem ser configuradas no arquivo docker-compose.yml.

Os serviços podem ser gerenciados pelo Docker através dos seus respectivos nomes, conforme legenda:
```
kb_lb -> NGINX Load Balancer
kc1 -> Keycloak Auth Server 1
kc2 -> Keycloak Auth Server 2
kc_db -> PostgreSQL Database
```

