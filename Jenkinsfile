node{
    stage("Git Clone"){
        git credentialsId: 'GIT_CREDENTIALS', url: 'https://github.com/gitsherin/helm-charts.git'
    }
    /**
    stage("Shell Command"){
        sh "chmod +x gke.sh"
        sh "./gke.sh"
    }
    **/
    /**
    stage("Create k8s Cluster"){
        sh "gcloud container clusters create usercluster --zone asia-east1-b"
    }
    **/
    /**
    stage("download and install kubectl"){
        sh "sudo apt-get update && sudo apt-get install -y apt-transport-https gnupg2"
        sh "curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add '-'"
        sh "echo deb https://apt.kubernetes.io/ kubernetes-xenial main | sudo tee -a /etc/apt/sources.list.d/kubernetes.list"
        sh "sudo apt-get update"
        sh "sudo apt-get install -y kubectl"
    }
    stage("Get Kubernetes Cluster Credentials"){
        sh "gcloud container clusters get-credentials usercluster --zone asia-east1-b"
    }
    **/
    /**
    stage("Helm Installation"){
        sh "curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3"
        sh "chmod 700 get_helm.sh"
        sh "./get_helm.sh"
    }
    **/
    stage("Install Helm Chart"){
        git credentialsId: 'GIT_CREDENTIALS', url: 'https://github.com/gitsherin/helm-charts.git'
        sh "helm install usersdata test/"
    }    
}
