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
        post {
        always {
            echo 'Pipeline finished'
            mail to: ivo.lazarov.97@gmail.com, subject: 'The Pipeline has finished'
        }
    }
    }
}
