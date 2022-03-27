# Microservices:  Python + Flask  => Dockerized ::: Deployed => Kubernetes + Helm

1. Create virtual environment  ` python -m venv microservices-python ` 

![image](https://user-images.githubusercontent.com/31022640/160261575-4e1622d6-08a1-43f5-ba84-8f69e06e6080.png)

2. Install Flask `pip install Flask`
3. Run `pip list` to inspect packages

![image](https://user-images.githubusercontent.com/31022640/160261535-dce84749-0a26-4946-9bf7-91a6ca706b66.png)

4. Flask application / Jinja templating 
5. Freeze Dependancies `pip freeze > requirements.txt`
6. Build Docker image
   When building image I encountered a stubborn error related to testing on local host. 
   standard build command: `docker build -t webapp:1.0` returned NewConnectionError.
   Solution: `docker build --network=host -t webapp:1.0 .` https://docs.docker.com/network/host/
8. Write Docker Compose file
9. Write Kubernetes Manifest files
10. Create HELM chart
