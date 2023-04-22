# 🔑 Keycloak Cluster

Keycloak cluster composed with Nginx as load balancer and PostgreSQL

<img  width="500" src="https://user-images.githubusercontent.com/90735184/158608991-10152f05-e6af-4f9e-b3d8-7e485b406908.png">

## 🚀 Technologies

* Docker
* Keycloak
* Nginx
* PostgreSQL

## ⚠️ Dependencies

**[Docker](https://www.docker.com/)**

## 🐳 Installation

Clone the repository:
```
git clone https://github.com/passosleo/keycloak-cluster-service.git
```

Navigate to project folder:
```
cd keycloak-cluster-service
```

Run the command below to build the cluster:
```
docker compose -f docker-compose.yml up
```

Access Keycloak panel in:
```
http://localhost:8000/
```

## 🖥️ Usage

The repository below provides a simple ReactJS front-end application integrated with Keycloak.

👉🏻 **[Keycloak React App](https://github.com/passosleo/keycloak-react-app)**
