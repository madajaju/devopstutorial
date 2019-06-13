pipeline {
  environment {
    DOCKER = credentials('dockerhub')
    REGISTRY = "madajaju"
  }
  agent {
    label 'dev'
  }
  stages {
    stage ('Build') {
      agent {
        label 'dev'
      }
      steps {
        sh 'cd services/inventory && docker build . -t madajaju/devops-inventory'
      }
    }
    stage ('BuildDocs') {
      agent {
        label 'dev'
      }
      steps {
        sh 'ls -latr'
      }
    }
    stage ('Test') {
      agent {
        label 'test'
      }
      steps {
        sh 'ls -latr'
      }
    }
    stage ('Publish') {
      agent {
        label 'dev'
      }
      steps {
        sh 'ls -latr'
      }
    }
    stage ('Deploy') {
      agent {
        label 'prod'
      }
      steps {
        sh 'ls -latr'
      }
    }
  }
}
