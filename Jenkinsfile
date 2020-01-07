pipeline {
  agent {
    node {
      label 'keen'
    }

  }
  stages {
    stage('Github Pull') {
      steps {
        git(url: 'https://github.com/techuy/test_automation_framework_v1', poll: true)
      }
    }

    stage('Check path') {
      steps {
        sh '''$PATH
ls'''
      }
    }

  }
}