pipeline {
    agent { 
        node {
            label 'kubeagent'
        }
    } 
    
    stages {
        stage('Example Build') {
            steps {
                echo "Hello"
            }
        }
        stage ('Cloning our Git') {
            steps { git branch: 'main',
                        credentialsId: 'github-pass',
                        url: 'https://github.com/Sicario7297/docker-test.git'
            }
        }
        stage('Testing connectivity to ArgoCD') {
            steps {
                echo "Rolling back" 
            }
        }
    }
}
