pipeline {
    agent any
    stages {
        stage('one') {
            steps {
                sh 'exit 1'
            }
        }
        stage('two') {
            steps {
                sh 'exit 0'   // failure
            }
        }
    }
    post {
        always {
            sh 'exit 0'
        }
    }
}
