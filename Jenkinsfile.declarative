pipeline {
    agent {
        node {
            label 'AGENT-1'
    }
}
    
    stages {
        stage('Build') {
            steps {
                echo "building"
            }
        }
        stage('Test') {
            steps {
                echo "Testing"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying"
            }
        }
    }
    post {
        always {
            echo 'I will always say Hello again!'
        }
    
        success {
            echo 'pipeline running success..!'
        }
        failure {
            echo 'pipeline runnig failure'
        }
    }
}