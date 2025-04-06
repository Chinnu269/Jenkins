pipeline {
  agent any
  environment {                                        //pipeline variable: All the stages of the pipeline can use it
    ENV_URL= "pipeline.google.com"              
  }
    stages {
        stage('stage1') {
            steps {
              sh '''
              echo Hello world
              echo welcome to jenkins
              echo environment variable is: ${ENV_URL}

              '''
            }
        }
        stage('stage2') {
            steps {
              sh "echo stage2 demo"
            }
        }
        stage('stage3') {
            steps {
              sh "echo stage3 demo"
            }
        }
    }
}