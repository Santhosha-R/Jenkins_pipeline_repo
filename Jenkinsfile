pipeline {
    agent any
    parameters {
        booleanparam(name: 'DEPLOY', description: 'wants to deploy production')
    }

    environment {
        CURRENT_ENV = 'prod'
    }

    stages {
        stage ('STAGE1 when branch main') {
            when {
                branch 'main'
            }
            steps {
                echo "This is satage1"
                sh '''
                    sleep 10'
                    EXIT 1
                '''
            }
        }
    
        stage('when environment') {
            when {
                environment name: 'CURRENT_ENV', value: 'prod'
            }
            steps {
                echo "This is WINDOWS testing"
                sh 'sleep 10'
            }               
        }
        stage('when parameter') {
            when {
                expression {params.DEPLOY == true}
            }
            steps {
                echo "This is WINDOWS testing"
                sh 'sleep 10'
            }               
        }
    }
}

        

