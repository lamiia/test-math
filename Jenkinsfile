pipeline {
  agent none
  stages {
    stage('Test') {
      agent {
        docker {
        image 'golang'
        }
      }
      steps {
        sh 'go test'
      }
    }
  stage('Deploy') {
    agent none
    steps {
      script {
        def customImage = docker.build("gdelanoy/maths:${env.BUILD_NUMBER}")
      }
    }
  }
}
}
