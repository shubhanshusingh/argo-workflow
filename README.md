Quick start setup local argo with minikube
-
https://argo-workflows.readthedocs.io/en/latest/quick-start/


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
