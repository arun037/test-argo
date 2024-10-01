pre-requisites:

an existing eks cluster

steps 1: kubectl create namespace argocd

step 2: kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

step 3: k get po,svc -n argocd

step 4: change the svc from clusterIP to loadBalancer

step 5: k -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d   --->  for decoding the password
