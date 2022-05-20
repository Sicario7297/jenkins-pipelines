pipeline {
  agent { label 'kubeagent' }
  stages {
    stage('Source') {
      steps {
        git 'https://github.com/digitalvarys/jenkins-tutorials.git'
      }
    }
    stage('Compile') {
      tools {
        gradle 'Default'
      }
      steps {
        sh 'gradle clean compileJava test'
      }
    }
  }
}
