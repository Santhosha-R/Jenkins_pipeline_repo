pipeline {
    agent any
    stages {
        stage ('STAGE1') {
            steps {
                echo "This is stage1 running"
                sh 'pwd'
            }
        }
        stage ('STAGE2') {
            steps {
                echo "This is stage2 running"
                sh 'ls'
            }
        }
        stage ('STAGE3') {
            steps {
                echo "This is stage3 running"
                sh 'whoami'
            }
        }
    }
}