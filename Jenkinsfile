pipeline {
    agent any
    def build_ok = true
    stages {       
        stage('one'){
           steps{
                  
              sh 'exit 0'
            }
         }
     
        try{
        stage('two') {
              steps{
            sh 'exit 1'   // failure
                  }
        }
    } catch(e) {
        build_ok = false
        echo e.toString()  
    }

        stage('one'){
           steps{
                  
              sh 'exit 0'
            }
         }
            if(build_ok) {
        currentBuild.result = "SUCCESS"
                     } else {
        currentBuild.result = "FAILURE"
                           }
    }
}
