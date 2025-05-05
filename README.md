# devops-sandbox
DevOps practices by developing, packaging, and deploying a demo web application from scratch. The project follows the complete Software Development Lifecycle (SDLC)

// local version
go build -o bin/app src/main.go - run to build proj
bin/app - run to start server on port :8080

// docker version
docker build .
docker run -p 8080:8080 sha256:tag_ref

// kubernetes version
curl -s https://raw.githubusercontent.com/k3d-io/k3d/main/install.sh | bash 
// or 
brew install k3d

k3d --version
k3d cluster create my-cluster
k3d cluster list
kubectl create deploy my-cluster --image yuriy123123/devops-sandbox:v1.0.0
kubectl get po -w
kubectl port-forward deploy/my-cluster 8080

kubectl get deploy my-cluster -o wide
kubectl set image deploy my-cluster devops-sandbox=yuriy123123/devops-sandbox:v1.0.1
kubectl get po -w
kubectl port-forward deploy/my-cluster 8080
// after
k3d cluster delete my-cluster
k3d cluster list