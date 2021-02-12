pipeline {
  environment {
    registry = "ctael5co/hello-app"
    registryCredential = 'dockerhub-ctael5co'
    dockerImage = ''
  }
  agent any
  stages {
    stage('Cloning Git') {
      steps {
        checkout scm
      }
    }
    stage('init') {
      steps {
        script {
          docker.image('hashicorp/terraform').inside("--entrypoint=''") {
          ansiColor('xterm') {
            sh 'curl github.com/meta'
          }
        }
      }
    }
  }
}
}
