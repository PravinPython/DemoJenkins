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

    stage('Docker Build') {
      steps {
        sh 'docker build -f Dockerfile .'
      }
    }

  }
}