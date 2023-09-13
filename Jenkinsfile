pipeline {
    
    agent none

    environment {
        COMPOSE_PROJECT_NAME = "${env.JOB_NAME}-${env.BUILD_ID}"
    }
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
        stage('Echo') {

            agent {
                dockerfile {
                    args '-u root:root'
                }
            }

            steps {
                
                echo sh(script: 'env|sort', returnStdout: true)

            }

        }
    }
}
