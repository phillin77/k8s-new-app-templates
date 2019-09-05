# Example from:  
- [https://github.com/kubernetes-sigs/kustomize/tree/master/examples/mySql](https://github.com/kubernetes-sigs/kustomize/tree/master/examples/mySql)  
- [https://codertw.com/資料庫/10331/](https://codertw.com/%E8%B3%87%E6%96%99%E5%BA%AB/10331/)

## Download example resources
        cd <your-project-dir>

        DEMO_HOME=$(pwd)

        CONTENT="https://raw.githubusercontent.com/phillin77/k8s-new-app-templates/master/MySQL"

        curl -s -o "$DEMO_HOME/#1.yaml" "$CONTENT/{mysql-deployment,mysql-service,mysql-secret,kustomization}.yaml"
