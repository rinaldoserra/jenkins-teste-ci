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
                    // alwaysPull false
                    // image 'microsoft/dotnet:2.2-sdk'
                    // reuseNode false
                    args '-u root:root'
                }
            }

            steps {
                
                echo sh(script: 'env|sort', returnStdout: true)

            }

        }


        stage('Sock') {

            agent {
                dockerfile {
                    args '-u root:root -v /var/run/docker.sock:/var/run/docker.sock'
                }
            }

            steps {


                     sh  ''' echo 'hajsaks' '''
                
            }

        }

 
    }
    post {

        always {
            node('main'){
                
                sh  '''
               
                '''
            }
        }
    }
}
