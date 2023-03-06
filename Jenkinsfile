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

    stage('Docker Bulid') {
      agent {
        node {
          label 'Environment'
        }

      }
      environment {
        DOCKERHUB_USER = 'praviningle9767@gmail.com'
        DOCKERHUB_PASSWORD = 'Coditation@1991'
      }
      steps {
        sh 'docker build .'
      }
    }

  }
}