pipeline {
  
  agent any
  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/nirmata-add-ons/demo-1.git', branch:'main'
      }
    }

    stage('Deploy App') {
      steps {
        sh 'sudo kubectl --kubeconfig=/root/.kube/config create -f nginx.yaml'
      }
    }

  }

}
