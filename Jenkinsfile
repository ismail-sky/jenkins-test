pipeline {
    agent any
    stages {
        stage('one') {
            steps {
                script {
                    //try {   
                      sh '''
                      echo $((54 / 0))
                      echo $?
                      '''
                   // }catch(Exception e){
                     //  error "exception and exit " 
                    //}
                
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
