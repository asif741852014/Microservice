pipeline {
    agent any

    stages {
        stage('Deploy To Kubernetes') {
            steps {
                withKubeCredentials(kubectlCredentials: [[caCertificate: '', clusterName: ' EKS-1', contextName: '', credentialsId: 'k8stoken', namespace: 'webapps', serverUrl: 'https://6BCE80061EFB6BCF6CB848A06061B6A9.gr7.ap-south-1.eks.amazonaws.com']]) {
                  sh "kubectl apply -f deployment-service.yml"
                    }
                    
                    
                }
            }
        
        
    }
}
