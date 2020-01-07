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
        sh '''cd "$PWD"/pt
jmeter -Jjmeter.save.saveservice.output_format=xml -n -t test.jmx -Jthreads=2 -l Report\\result.jtl'''
      }
    }

    stage('Report') {
      steps {
        perfReport 'Report/result.jtl'
      }
    }

  }
}