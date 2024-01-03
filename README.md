# python-flask-restapi
Example Project on how to develop RESTful API with Flask and Python



// clone the project
git clone https://github.com/bbachi/python-flask-restapi.git

// change directory
cd python-flask-restapi// build the image

docker build -t flask-restapi .// list the image

docker images


Run the container

// run the container

docker run -d -p 5000:5000 --name python-restapi flask-restapi// list the container

docker ps// logs


docker logs python-restapi// exec into running container


docker exec -it python-restapi /bin/sh

#check in browser :  127.0.0.1:5000  or  localhost:5000 

# Minikube 

minikube start


kubectl create -f pod.yml

// get the pod

kubectl get po// exec into running pod

kubectl exec -it pythonapi /bin/sh

// deployments

kubectl create -f deployment.yml

kubectl get deploy

kubectl get pods --> show all running pods with replicas


kubectl create -f service.yml

kubectl get svc    ---->  show ports in PORTS section     5000:31672 in my project.


kubectl cluster-info ----> show Cluster IP . My Cluster IP : 192.168.64.2

// access the application here in browser

http://192.168.64.2:31672/api/tasks
