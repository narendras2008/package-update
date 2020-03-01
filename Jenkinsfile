pipeline {
    agent any
       stages {
           stage('package update in DTL Agent') {
               agent {
                   node {
                       label("DTL-LIN1")
                   }
               }
               steps {
                   sh 'sudo yum update -y'
               }
           }
           stage('package update in prod agent') {
               agent {
                   node {
                       label("PROD-LIN1")
                        }
                      }
               steps {
                   sh 'sudo yum update -y'
               }
           }
       }
        post {
          always {
             cleanWs()
                 }
              }
    }
