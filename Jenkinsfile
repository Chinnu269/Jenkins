pipeline {
  agent any
  environment {                                        //pipeline variable: All the stages of the pipeline can use it
    ENV_URL= "pipeline.google.com"  
    SSH_CRED = credentials('SSH_CRED')              
  }
   triggers {
        pollSCM('*/1 * * * 0-5')
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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