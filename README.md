# devops-sandbox
DevOps practices by developing, packaging, and deploying a demo web application from scratch. The project follows the complete Software Development Lifecycle (SDLC)

// local version
go build -o bin/app src/main.go - run to build proj
bin/app - run to start server on port :8080

// docker version
docker build .
docker run -p 8080:8080 sha256:tag_ref