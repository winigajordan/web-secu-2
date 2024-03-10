pipeline {
   agent { 
     docker { image 'jenkins/jenkins:alpine3.19-jdk21' }
  }
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('Build') {
            steps {
                echo "Building.."
                sh '''
                echo "doing build stuff.."
                '''
            }
        }
  }
}
