pipeline {
  agent any

  stages {

    stage('Build Docker Image') {
      steps {
        sh 'docker build -t myapp .'
      }
    }

    stage('Deploy to Kubernetes') {
      steps {
        sh 'kubectl apply -f deployment.yaml'
      }
    }
  }
}
