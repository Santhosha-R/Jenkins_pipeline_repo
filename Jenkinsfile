pipeline {
    agent any
    stages {
        stage ('STAGE1') {
            steps {
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
                    echo "This is satage1"
                    sh ''' 
                        sleep 10
                        exit 1
                        '''
                }
            }
        }
        stage('PARALLEL TESTING') {
            parallel {
                stage('WINDOWS TESTING') {
                    steps {
                        echo "This is WINDOWS testing"
                        sh 'sleep 10'
                    }               
                }
                stage('MACOS TESTING') {
                    steps {
                        echo "This is MACOS testing"
                        sh 'sleep 10'
                    }                
                }
            }
        }
        stage('FINALLy TESTING') {
            steps {
                echo "This is FINALLY testing"
                sh 'sleep 10'
            }
                
        }
    }
}
