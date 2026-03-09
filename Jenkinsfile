pipeline {
    agent { label 'slave2'}
    stages {
        stage ('STAGE1') {
            steps {
                echo "This is stage1 running"
                sh '''
                    pwd
                    sleep 5
                '''
            }
        }
        stage ('STAGE2') {
            steps {
                echo "This is stage2 running"
                sh '''
                    ls
                    sleep 5
                '''
            }
        }
        stage ('STAGE3') {
            steps {
                echo "This is stage3 running"
                sh '''
                    whoami
                    sleep 5
                '''
            }
        }
    }
}