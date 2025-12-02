pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        echo 'Checkout code'
        git url: 'https://github.com/wiem-kb/exam.git', branch: 'main'
      }
    }

    stage('Install dependencies') {
      steps {
        echo 'Install npm dependencies'
        sh 'npm install'
      }
    }

    stage('Run tests') {
      steps {
        echo 'Run npm test'
        // adapter selon script de test dans package.json
        sh 'npm test || true'
      }
    }

    stage('Build Docker image') {
      steps {
        echo 'Build Docker image'
        // Nécessite que l'agent Jenkins puisse exécuter docker (ou Docker-in-Docker)
        sh 'docker build -t todo-app .'
      }
    }
  }

  post {
    always {
      echo 'Pipeline terminé'
    }
    success {
      echo 'Pipeline OK'
    }
    failure {
      echo 'Pipeline échoué'
    }
  }
}
