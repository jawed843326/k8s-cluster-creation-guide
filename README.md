Commands used during hands-on practice

docker ps	List running containers
docker ps -a	List all containers (running + stopped)
docker images	List local images
docker run -it --name mycontainer ubuntu bash	Start a new container interactively with bash
docker stop <container>	Stop a running container
docker start <container>	Start a stopped container
docker restart <container>	Restart a container
docker rm <container>	Delete a container
docker rmi <image>	Delete an image
docker logs <container>	View logs of a container
docker exec -it <container> bash	Open shell in running container
docker build -t myimage:tag .	Build image from Dockerfile
2️⃣ Kind Commands (Kubernetes in Docker)
Command	Description
kind create cluster	Create a new kind cluster
kind create cluster --name <name> --config <file>	Create a cluster with custom config (multi-node, port mappings)
kind get clusters	List all kind clusters
kind delete cluster --name <name>	Delete a kind cluster
docker ps	View kind nodes (they are Docker containers)
docker pause <node>	Pause a node (stop it temporarily)
docker unpause <node>	Resume a paused node
kubectl get nodes	Verify nodes in the kind cluster
kind export kubeconfig --name <name>	Export kubeconfig for this cluster
3️⃣ Kubernetes (kubectl) Commands
Command	Description
kubectl get nodes	List cluster nodes
kubectl get pods	List pods in current namespace
kubectl get pods -o wide	List pods with node info and IP
kubectl get svc	List services
kubectl get deployments	List deployments
kubectl describe pod <pod>	Detailed info about a pod
kubectl logs <pod>	View pod logs
kubectl exec -it <pod> -- bash	Open shell in pod
kubectl delete pod <pod>	Delete a pod (Deployment auto-recreates it)
kubectl apply -f <file.yaml>	Create/update resources from YAML
kubectl delete -f <file.yaml>	Delete resources from YAML
kubectl get ingress	List ingress resources
`kubectl port-forward <pod	svc> <localPort>:<containerPort>`
kubectl cordon <node>	Mark node unschedulable
kubectl drain <node>	Evict pods from node safely
kubectl uncordon <node>	Make node schedulable again
kubectl get events	View cluster events for troubleshooting
kubectl get all	List all resources in current namespace
