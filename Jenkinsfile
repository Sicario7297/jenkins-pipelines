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
        gradle 'gradle7'
      }
      steps {
        sh 'gradle clean compileJava test'
      }
    }
  }
}
