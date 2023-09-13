pipeline {
  agent any
  stages {
    stage('compilando') {
      steps {
        sh 'echo Building ${BRANCH_NAME}...'
      }
    }
    stage('testando') {
      steps {
        sh 'echo Teste ${BRANCH_NAME}...'
      }
    }
    stage('publicando') {
      steps {
        sh 'echo Public ${BRANCH_NAME}...'
      }
    }
  }
}
