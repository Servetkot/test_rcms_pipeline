pipeline {
  agent any
  stages {
    stage('input1') {
      steps {
        withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId:
        'meggp.vipa.uk.ibm.com', usernameVariable: 'mysecretusername',
        passwordVariable: 'mysecretpassword']]) {
          input(message: 'is it input', ok: 'oga')
          sh 'echo "hello world $mysecretusername"'
        }
      }
    }
    stage('input2') {
      steps {
        withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId:
        'meggp.vipa.uk.ibm.com', usernameVariable: 'mysecretusername',
        passwordVariable: 'mysecretpassword']]) {
        echo 'hello 2'
        input(message: 'is it second input?', ok: 'yea')
        sh 'echo "goodbay"'
        }
      }
    }
  }
}
