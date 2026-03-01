# k8FIrstProject
First time getting hands on expirence with Kubernetes 

---------Features---------
- Flask web app returning “Hello Kubernetes!”
- Dockerized for containerized deployment
- Kubernetes Deployment to manage app replicas
- Kubernetes Service of type LoadBalancer to expose the app

-------Kubernetes Concepts Demonstrated----------
- Deployment: Automatically manages app replicas
- Service: Exposes app to external traffic
- Containerization: Docker image for portability
- LoadBalancer: Simple way to make the app publicly accessible

--------Lessons Learned-----------
How to containerize a simple Python app with Docker
Basic Kubernetes objects (Deployment, Service)
How to deploy and expose a web app in Kubernetes
Importance of specifying container ports and mapping them correctly

-------Architecture Diagram-------

+--------------------+
|   User / Browser   |
+--------------------+
           |
           v
+--------------------+
|   Service          |  <-- Type: LoadBalancer
| simple-webapp-svc  |
+--------------------+
           |
           v
+--------------------+
| Deployment         |
| simple-webapp      |  <-- Replica of Flask container
+--------------------+
           |
           v
+--------------------+
| Docker Container   |
| Flask App (5051)   |
+--------------------+
