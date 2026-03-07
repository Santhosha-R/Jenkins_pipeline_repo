pipeline {
    agent any

    environment {
        DOCKER_USER = 'Tejasthu'
        AWS_ACESS_KEY = '9113675170'

    }
    stages {
        stage ('STAGE1') {
            
            environment {
                STAGE = 'stage1'
            }

            steps {
                echo " DOCKER_USER: ${env.DOCKER_USER}"
                echo " AWS_ACESS_KEY: ${env.AWS_ACESS_KEY}"
                echo " STAGE: ${env.STAGE}"

                sh '''
                    env
                '''
            }
        }
        stage ('STAGE2') {

            steps {
                echo " DOCKER_USER: ${env.DOCKER_USER}"
                echo " AWS_ACESS_KEY: ${env.AWS_ACESS_KEY}"
                echo " STAGE: ${env.STAGE}"

                sh '''
                    env
                '''
            }
        }
    }
}