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
        sh 'sudo kubectl --kubeconfig=/root/.kube/config create -f /var/lib/jenkins/workspace/demo-2022/nginx.yaml'
      }
    }

  }

}
