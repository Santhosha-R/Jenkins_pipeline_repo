pipeline {
    agent any

    environment {
        DOCKER_USER = 'santhu'
        AWS_ACESS_KEY = '9113675170'

    }
    stages {
        stage ('STAGE1') {

            steps {
                echo " DOCKER_USER: ${env.DOCKER_USER}"
                echo " AWS_ACESS_KEY: ${env.AWS_ACESS_KEY}"

                sh '''
                    env
                '''
            }
        }
    }
}