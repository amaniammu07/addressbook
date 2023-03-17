pipeline {
    agent any
    stages {
        stage('Compile') {
            steps { 
                sh 'mvn compile'
            }
        }
        stage('test') {
            steps { 
                sh 'mvn test'
            }
        }
        stage('package') {
            steps { 
                sh 'mvn package'
            }
        }
    }
  post {
  success {
    // One or more steps need to be included within each condition's block.
  }
  failure {
    // One or more steps need to be included within each condition's block.
        }
     }   
  }

