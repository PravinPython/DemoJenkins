pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/PravinPython/DemoJenkins.git', branch: 'main')
      }
    }

    stage('Log') {
      steps {
        sh 'ls -la'
      }
    }

    stage('Build') {
      steps {
        sh 'docker build -f Dockerfile . -t praviningle/jenkins1-demo:latest'
      }
    }

    stage('Login to DockerHub') {
      environment {
        DOCKERHUB_USER = 'praviningle'
        DOCKERHUB_PASSWORD = 'Coditation@1991'
      }
      steps {
        sh 'docker login -u $DOCKERHUB_USER -p $DOCKERHUB_PASSWORD'
      }
    }

    stage('Push') {
      steps {
        sh 'docker push praviningle/jenkins1-demo:latest'
      }
    }

  }
}