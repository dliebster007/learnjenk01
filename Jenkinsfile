pipeline {
  agent any
  stages {
    stage('one') {
      steps {
        sh 'date |tee date.out'
      }
    }
    stage('two') {
      steps {
        echo 'second step'
      }
    }
    stage('nancy') {
      steps {
        isUnix()
      }
    }
    stage('BuildMe') {
      steps {
        build 'SampleBuildJob'
      }
    }
  }
}