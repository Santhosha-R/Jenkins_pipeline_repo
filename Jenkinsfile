pipeline {
    agent any
    stages {
        stage ('STAGE1') {
            steps {
                echo " This is stage 1"

                sh '''
                    sleep 5
                    echo "This is linux command"
                 '''
            }
        }
        stage ('STAGE2') {
            steps {
                 echo " This is stage 2"

                 sh '''
                    #!/bin/bash
                    pwd
                    ls -lrt
                    sleep 5
                 '''
            }
        }
    }

}
