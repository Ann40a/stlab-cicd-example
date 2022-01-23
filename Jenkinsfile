pipeline {
  agent { docker { image 'golang:1.17.6-alpine' } }
  stages {
    stage('Build') {
      steps {
        sh 'go build'
      }
    }
  }
}
