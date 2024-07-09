Quick start setup local argo with minikube
-
https://argo-workflows.readthedocs.io/en/latest/quick-start/


Build the image using dockerfile

``
docker build -t argo-workflow .
``

or


``
podman build -t argo-workflow .
``

Push the image to minikube cluster

``
minikube image load argo-workflow
``

submit argo workflow in argo namespace

single step workflow 

``
argo submit -n argo --watch argo-workflow.yaml
``

multi step workflow

``
argo submit -n argo --watch argo-workflow-multi-step.yaml
``