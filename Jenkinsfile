pipeline {
  
    options {
    ansiColor('xterm')
  }

  agent { label 'kubepod' }

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/nirmata-add-ons/demo-1.git', branch:'main'
      }
    }

    stage('Deploy App') {
      steps {
        sh 'kubectl apply -f nginx.yaml'
      }
    }

  }

}
