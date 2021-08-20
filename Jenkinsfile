pipeline {
    agent any
    stages {
        stage('one') {
            steps {
                script {
                    try {   
                      sh '2/4'
                    }catch(e){
                       error "exception "
                    }
                
                }
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
            //sh 'exit 0'
            echo 'One way or another, I have finishedwith failure stage'
        }
    }
}
