pipeline {
  agent any
  stages {
    stage('provision node') {
      steps {
        node(label: 'kubernetes')
      }
    }
    stage('ut') {
      parallel {
        stage('ut') {
          steps {
            sleep 600
          }
        }
        stage('') {
          steps {
            sleep 100
          }
        }
      }
    }
    stage('stg') {
      steps {
        dir(path: '/')
      }
    }
  }
  environment {
    stg = 'stg'
  }
}