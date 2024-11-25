pipeline {
     agent any
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

