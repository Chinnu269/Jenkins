pipeline {
  agent any
  environment {                                        //pipeline variable: All the stages of the pipeline can use it
    ENV_URL= "pipeline.google.com"  
    SSH_CRED = credentials('SSH_CRED')             
  }
    stages {
        stage('stage1') {
            steps {
              sh '''
              echo Hello world
              echo welcome to jenkins
              echo environment variable is: ${ENV_URL}
              env

              '''
            }
        }
        stage('stage2') {
        environment {
            BATCH= "B55"
        } 
            steps {
              sh "echo stage2 demo"
              sh "echo devops batch is: ${BATCH}"
            }
        }
        stage('stage3') {
            steps {
              sh "echo stage3 demo"
            }
        }
    }
}