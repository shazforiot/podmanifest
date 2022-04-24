pipeline{
    agent any
    stages{
        stage('Checkout Source'){
            steps{
                git 'https://github.com/KrishnaPrakash650/podmanifest.git'
            }
        }
        stage('Deploying App to Kubernetes'){
            steps{
                script{
                    KubernetesDeploy(configs: "podmanifest.yml", kubeconfigID: "kubernetes")
                }
            }
        }
    }
}