pipeline {
     agent any
environment {
         DOCKER_IMAGE = 'hello-py:latest' //dokcer image name
 }
 stages {
     stage('Checkout') {
         steps {
              checkout scm
            }
        }
     stage('Run Hello World') {
            steps {
                sh 'python3 hello.py'
            }
        }
     stage('Docker Build') {
         steps {
            sh """
            docker build -t $DOCKER_IMAGE .
              """
           }
         }
}
 post {
         success {
              echo ' successfully .'
           }
         failure {
              echo 'failed'
             }
         }
    }

