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

    stage('Check path') {
      parallel {
        stage('Check path') {
          steps {
            sh '''$PATH
'''
          }
        }

        stage('') {
          steps {
            sh 'ls'
          }
        }

      }
    }

  }
}