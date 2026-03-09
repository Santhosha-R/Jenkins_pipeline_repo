pipeline {
    agent any
    stages {
        stage ('STAGE1') {
            steps {
                echo "This is stage1 running"
                sh '''
                    pwd
                    sleep 10
                '''
            }
        }
        stage ('STAGE2') {
            steps {
                echo "This is stage2 running"
                sh '''
                    ls
                    sleep 10
                '''
            }
        }
        stage ('STAGE3') {
            steps {
                echo "This is stage3 running"
                sh '''
                    whoami
                    sleep 10
                '''
            }
        }
    }
}