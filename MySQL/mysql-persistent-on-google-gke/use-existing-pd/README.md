# Type of PersistentVolume  
Using preexisiting Persistent Disks as PersistentVolumes

## Download example resources
        cd <your-project-dir>

        DEMO_HOME=$(pwd)

        CONTENT="https://raw.githubusercontent.com/phillin77/k8s-new-app-templates/master/MySQL/mysql-persistent-on-google-gke/use-existing-pd"

        curl -s -o "$DEMO_HOME/#1.yaml" "$CONTENT/{mysql-pv,mysql-deployment,mysql-service,mysql-secret,kustomization}.yaml"

## Change the size and name of your PD in PersistentClaim
        (edit mysql-pv.yaml)
        (依據實際狀況修改好檔案中 TODO: 標注的設定值)

## Create K8S App (using kustomization)
        cd <your-project-dir>
        kubectl config get-contexts  # to get your context list
        kubectl config use-context <your context name for gke>
        kubectl apply -k ./  # kustomization.yaml 所在的目錄
