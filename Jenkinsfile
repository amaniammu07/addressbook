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
      body: '${BUILD_NUMBER}',subject: 'build completed with status ${BUILD_STATUS}', to: 'amaniammu2101@gmail.com'
  }
  failure
      {
          body: '{BUILD_NUMBER}',subject: 'build has completed with status ${BUILD_STATUS}', to: 'amaniammu2101@gmail.com'
      } 
  }
}
