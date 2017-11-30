pipeline {
  agent none
  stages {
    stage('testing') {
      agent {
        docker {
          image 'golang'
        }
      }
      steps {
        sleep 2
        sh 'go test'
      }
    }
  }
}
