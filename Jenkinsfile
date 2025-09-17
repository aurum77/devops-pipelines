pipeline {
  agent {
    docker { image 'node:22.19.0-alpine3.22' }
  }
  stages {
    stage('Pull') {
      steps {
        git branch: 'main',
            url: 'https://github.com/aurum77/devops-pipelines.git'
      }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
  }
}
