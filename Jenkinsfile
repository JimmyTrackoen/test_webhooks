pipeline {
    agent any
    
    triggers {
        GenericTrigger(
            genericVariables: [
                [key: 'ref', value: '$.ref']
            ],

            causeString: 'Triggered on $ref',

            token: '123456',
            tokenCredentialId: '',

            printContributedVariables: false,
            printPostContent: false,
            silentResponse: false,

            regexpFilterText: '$ref',
            regexpFilterExpression: 'refs/heads/' + BRANCH_NAME
        )
    }
    
    stages {
        
        stage('Remote connection [only prod]'){
            when {
                branch 'main'
            }

            steps {
                echo 'run this stage - ony if the branch = master main'
            }
        }
        
        stage('Clone repository') {
            steps {
                sh 'echo "We clone repository :) !!!"'
            }
        }

        stage('Down services'){
            steps {
                sh 'echo Hello : `seq 1 10`'
            }
        }

        stage('Start db'){
            steps {
                sh 'echo Hello : `seq 1 10`'
            }
        }
        
        stage('Build/Package services'){
            steps {
                sh 'echo Hello : `seq 1 10`'
            }
        }
        
        stage('Start services'){
            steps {
                sh 'echo Branch Finded : $ref'
            }
        }
    }
}
