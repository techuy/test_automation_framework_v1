pipeline {
  agent {
    node {
      label 'keen'
    }

  }
  stages {
    stage('Git Pull') {
      steps {
        git 'https://github.com/techuy/test_automation_framework_v1'
      }
    }

    stage('Performance Test') {
      steps {
        build 'Performance_Testing'
      }
    }

  }
}