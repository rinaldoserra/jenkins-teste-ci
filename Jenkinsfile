pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo Building ${BRANCH_NAME}...'
      }
    }
    stage('test') {
      steps {
        sh 'echo Teste ${BRANCH_NAME}...'
      }
    }
    stage('public') {
      steps {
        sh 'echo Public ${BRANCH_NAME}...'
      }
    }
  }
}
