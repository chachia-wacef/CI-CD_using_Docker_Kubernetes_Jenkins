# CI-CD_using_Docker_Kubernetes_Jenkins

This project aims to automate the creation, testing (continuous integration) and deploy (continuous deployment) our project filed on GitHub. It consists in testing the code, build the docker image, pusher it in dockerHub and finally deploy it on a kubernetes cluster already created.

To integrate Jenkins with Kubernetes, we need to install 2 plugins on jenkins. The first one is "Docker pipeline" which allows to build, test and use Docker images from Jenkins Pipeline projects (allows us to mount Jenkins workspace as a "volume" inside the container, using the same file path). The second is "Kubernetes Continious deploy" which allows us to deploy resource configurations to a Kubernetes cluster. In our project we already have a Kubernetes cluster that contains running nodes, and we want to automate the relaunch of new nodes when the docker images of the applications are modified.
