pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'Echo Building ${BRANCH_NAME}...'
      }
    }
    stage('test') {
      steps {
        sh 'Echo Teste ${BRANCH_NAME}...'
      }
    }
    stage('public') {
      steps {
        sh 'Echo Public ${BRANCH_NAME}...'
      }
    }
  }
}
