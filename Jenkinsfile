pipeline {
  agent any
  def app
  stages {
    stage('---clone repo---') {
      steps {
        checkout scm
      }
    }
    stage('Build image'){
      steps {
        app = docker.build("arwamohsen/airportapp")
}
}
    stage('push image') {
      steps {
        docker.withRegistry('https://registry.hub.docker.com', 'docker-hub') {
          app.push("${env.BUILD_NUMBER}")
          app.push("latest")
}
}
  }
}
}
