pipeline {
  agent any
  stages {
    stage('Checkout') {
      parallel {
        stage('Checkout') {
          steps {
            echo 'Checkout code from repository'
          }
        }
        stage('ProjectA') {
          steps {
            echo 'Checking out ProjectA'
          }
        }
        stage('ProjectB') {
          steps {
            echo 'Checking out ProjectB'
          }
        }
      }
    }
    stage('Build') {
      steps {
        echo 'Building project '
      }
    }
    stage('Run Tests') {
      parallel {
        stage('Run Tests') {
          steps {
            echo 'Executing tests'
          }
        }
        stage('Functional') {
          steps {
            echo 'Running functional tests'
          }
        }
        stage('Performace') {
          steps {
            echo 'Running performance tests'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying Project'
      }
    }
  }
}