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

    stage('DockerHub Login') {
      environment {
        DOCKERHUB_USER = 'praviningle'
        DOCKERHUB_PASSWORD = 'Coditation@1991'
      }
      steps {
        sh 'docker login -u $DOCKERHUB_USER -P $DOCKERHUB_PASSWORD'
      }
    }

  }
}