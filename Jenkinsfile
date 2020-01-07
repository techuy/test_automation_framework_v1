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
      steps {
        sh '''cd "$PWD"/pt
jmeter -n -t test.jmx -Jthreads=2 -l Report\\result.jtl'''
      }
    }

    stage('') {
      steps {
        perfReport 'Report\\result.jtl'
      }
    }

  }
}