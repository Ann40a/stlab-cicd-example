pipeline {
  agent any
  stages {
    stage('Check golang version') {
      steps {
        bat 'go version > go-version.txt'
      }
    }
    stage('Test') {
      steps {
        bat 'go clean -testcache'
        bat 'go test ./...'
      }
    }
    stage('Build') {
      steps {
        bat 'go build'
      }
    }
  }
  post {
    always {
      archiveArtifacts 'go-version.txt'
    }
    success {
      archiveArtifacts '*.exe'
    }
  }
}
