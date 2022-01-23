pipeline {
  agent { docker { image 'golang:1.17.6-alpine' } }
  stages {
    stage('Test') {
      steps {
        sh 'go clean -testcache'
        sh 'go test ./...'
      }
    }
    stage('Build') {
      steps {
        sh 'go build'
      }
    }
  }
}
