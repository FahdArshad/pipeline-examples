pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        parallel(
          "build": {
            sh 'echo "$test"'
            
          },
          "build 2": {
            sh 'echo "$test2"'
            
          }
        )
      }
    }
    stage('final') {
      steps {
        timeout(time: 5) {
          echo 'hello'
        }
        
      }
    }
  }
  environment {
    test = '5'
    test2 = '10'
  }
}