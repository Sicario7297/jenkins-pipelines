pipeline {
    agent any
    stages {       
        stage ('testing') {
             steps {
                     echo "Successfull"
            }
        }
        stage ('pulling an image') {
             steps {
                     docker login -u '51c4r10' -p 'MyNameIsS1C4R10' 
                     docker pull busybox
                     echo "Success"
            }
        }
    }
}

