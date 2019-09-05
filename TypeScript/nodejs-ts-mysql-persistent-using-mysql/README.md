# nodejs-ts-mysql-persistent-using-mysql

TypeScript (Node.js ONLY, NO DATABASE) Kubernetes App Example

## Download example resources
        cd <nodejs-ts-mysql-persistent-using-mysql dir>

        DEMO_HOME=$(pwd)

        CONTENT="https://raw.githubusercontent.com/phillin77/k8s-new-app-templates/master/TypeScript/nodejs-ts-mysql-persistent-using-mysql"

        curl -s -o "$DEMO_HOME/#1.yaml" "$CONTENT/{mysql-deployment,mysql-secret,mysql-service,nodejs-ts-mysql-persistent-using-mysql-deployment,nodejs-ts-mysql-persistent-using-mysql-service,kustomization}.yaml"

## Create K8S App
        cd <nodejs-ts-mysql-persistent-using-mysql dir>
        kubectl config get-contexts  # to get your context list
        kubectl config use-context <your context name>
        kubectl apply -k ./

## Delete this K8S App
        cd <nodejs-ts-mysql-persistent-using-mysql dir>
        kubectl config get-contexts  # to get your context list
        kubectl config use-context <your context name>
        kubectl delete -k ./

## Test this K8S App on local machine
        kubectl get pods
        kubectl port-forward <pod name> 8080:8080

        curl http://loalhost:8080/
        curl http://loalhost:8080/mysql
