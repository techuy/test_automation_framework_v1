pipeline {
  agent none
  stages {
    stage('Github Pull') {
      steps {
        git(url: 'https://github.com/techuy/test_automation_framework_v1', poll: true)
      }
    }

    stage('') {
      steps {
        sh '$PATH'
      }
    }

  }
}