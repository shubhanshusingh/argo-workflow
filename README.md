Build the image using dockerfile

``
docker build -t argo-workflow .
``

Push the image to minikube

``
minikube image load <image name>
``

submit argo workflow in argo namespace

``
argo submit -n argo --watch argo-workflow.yaml
``
