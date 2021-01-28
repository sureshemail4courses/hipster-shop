pipeline {

  agent any
  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/sureshemail4courses/hipster-shop.git', branch:'master'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          sh 'sudo /usr/local/bin/kubectl apply -f release/kubernetes-manifests.yaml -n shopping'
        }
      }
    }

  }

}
