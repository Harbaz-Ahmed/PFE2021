pipeline {
  agent any
  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/Hbz-one/PFE2021.git'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
