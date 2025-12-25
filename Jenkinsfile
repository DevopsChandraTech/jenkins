pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }

    environment {
        COURSE = 'Jenkins'
    }

    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 10, unit: 'SECONDS')
        disableConcurrentBuilds()
    }

    stages {
        stage('build') {
            steps {
                script {
                    sh  """
                        echo 'Building the pipeline'
                        echo '$COURSE'
                        sleep 10
                    """
              }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh  """
                        echo 'Testing the pipeline'
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh  """
                        echo 'Deploying the pipeline'
                    """
                }
            }
        }
    }    
    post {
        always {
            echo 'pipeline running always '
        }
        success {
            echo 'if success'
        }
        failure {
            echo 'if failure'
        }
        aborted {
            echo 'aborted'
        }
    }
}