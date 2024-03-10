pipeline {
   agent { 
     docker { image 'jenkins/jenkins:alpine3.19-jdk21' }
  }
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('Test ') {
            steps {
                sh '''
                echo "Test Jenkins"
                '''
            }
    }
    stage('Scan') {
      steps {
        withSonarQubeEnv(installationName: 'sq1') { 
            sh './mvnw clean package sonar:sonar'
        }
      }
    }
    stage('Finised ') {
            steps {
                sh '''
                echo "Tout est OK"
                '''
            }
    }
  }
}
