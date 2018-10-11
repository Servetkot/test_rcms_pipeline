pipeline {
  agent any
  stages {
    stage('input1') {
      steps {
        input(message: 'is it input', ok: 'yes')
        sh 'echo "hello world"'
      }
    }
    stage('input2') {
      steps {
        echo 'hello 2'
        input(message: 'is it second input?', ok: 'yea')
        sh 'echo "goodbay"'
      }
    }
  }
}