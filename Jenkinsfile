pipeline {
    agent any

    triggers {
        pollSCM (H/3 * * * *)
    }
    parameters {
        booleanParam(name: 'DEPLOY', description: 'wants to deploy production')
    }

    environment {
        CURRENT_ENV = 'prod'
    }

    stages {
        stage ('CHECKOUT') {
            steps {
                git branch: 'main', 
                credentialsId: 'HP-git', 
                url: 'https://github.com/Santhosha-R/Tejasthu.git'
                
                // sh '''
                //     echo GIT_BRANCH: $GIT_BRANCH
                //     echo BRANCH_NAME: $BRANCH_NAME

                // '''            
            }
        }              
    
        stage ('STAGE1 when branch main') {
            when {
                expression {
                    return env.GIT_BRANCH == 'origin/santhu'
                }
            }
            steps {
                echo "This is satage1"
                sh '''
                    pwd
                    ls -lrt
                    sleep 10
                '''
            }
        }
    
        stage('when environment') {
            when {
                environment name: 'CURRENT_ENV', value: 'prod'
            }
            steps {
                echo "This is environment testing"
                sh 'sleep 10'
            }               
        }
        stage('when parameter') {
            when {
                expression {params.DEPLOY == true}
            }
            steps {
                echo "This is parameter testing"
                sh 'sleep 10'
            }               
        }
    }
}

        

