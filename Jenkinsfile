pipeline {
  agent any

  stages {

    stage('Clone') {
      steps {
        git 'https://github.com/AmeyaSRM/my-devops-app.git'
      }
    }

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
