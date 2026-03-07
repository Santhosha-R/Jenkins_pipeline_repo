pipeline {
    agent none

    parameters {
        string(name: "NAME",defaultValue:"",description:"please tell me your name")
        booleanParam(name: "SKIP_TEST",defaultValue:"false",description:"want to skip test run to direct deploy")
        choice(name: "BRANCH",choices:["master","stagging","prod"],description:"")
    }
    stages {
        stage ('STAGE1') {
            agent { label 'master'}

            steps {
                echo " NAME: ${params.NAME}"
                echo " SKIP_TEST: ${params.SKIP_TEST}"
                echo " BRANCH TO DEPLOY: ${params.BRANCH}"

                sh '''
                    echo " NAME: ${NAME}"
                    echo " SKIP_TEST: ${SKIP_TEST}"
                    echo " BRANCH TO DEPLOY: ${BRANCH}"

                '''
            }
        }
    }
}