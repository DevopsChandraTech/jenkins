pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }

    stages {
        stage('build') {
            steps {
                script {
                    sh  """
                        'Building the pipeline'
                    """
              }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh  """
                        'Testing the pipeline'
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh  """
                        'Deploying the pipeline'
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
    }
}