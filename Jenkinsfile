pipeline {
  agent none
  stages {
    stage('Performance Test') {
      steps {
        sh 'jmeter Jjmeter.save.saveservice.output_format=xml -n -t $path\\pt.jmx -l Test.jtl'
        perfReport(sourceDataFiles: '**/*.jtl', compareBuildPrevious: true)
      }
    }

  }
}