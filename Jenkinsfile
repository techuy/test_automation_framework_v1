pipeline {
  agent {
    node {
      label 'keen'
    }

  }
  stages {
    stage('Performance Test') {
      steps {
        build 'Performance_Testing'
      }
    }

  }
}