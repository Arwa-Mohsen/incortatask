pipeline {
  agent any
  stages {
    stage('---clean---') {
      steps { 
        sh "sudo docker build . -t airportapp:latest"
      }
    }
  }
}
