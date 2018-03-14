pipeline {
  agent any
  stages {
    stage('one') {
      parallel {
        stage('one') {
          steps {
            sh 'date |tee date.out'
          }
        }
        stage('') {
          steps {
            build 'SampleTestJob'
          }
        }
      }
    }
    stage('two') {
      parallel {
        stage('two') {
          steps {
            echo 'second step'
          }
        }
        stage('farf') {
          steps {
            sh 'date'
          }
        }
        stage('foof') {
          steps {
            sleep 2
            sh 'date'
          }
        }
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