pipeline {
  environment {
    DOCKER = credentials('dockerhub')
    REGISTRY = "madajaju"
  }
  stages {
    stage ('Build') {
      agent {
        label 'dev'
      }
      stage('inventory') {
        steps {
          sh 'cd services/inventory && docker build . -t madajaju/devops-inventory'
        }
      }
    }
    stage ('BuildDocs') {
      agent {
        label 'dev'
      }
      steps {
        sh 'ls -latr'
        sh 'echo "MADE IT" '
      }
    }
    stage ('Test") {
      agent {
        label 'test'
      }
    }
    stage ('Publish") {
      agent {
        label 'dev'
      }
    }
    stage ('Deploy") {
      agent {
        label 'prod'
      }
    }
  }
}
