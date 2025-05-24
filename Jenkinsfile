pipeline {
  agent any
  tools {
    nodejs 'node18'
  }

  options {
    timeout(time: 2, unit: 'MINUTES')
  }

  stages {
    stage('Install dependencies') {
      steps {
        bat 'cd devops && npm i'
      }
    }
    stage('Run tests') {
      steps {
        bat 'cd devops && npm t'
      }
    }
  }
}
