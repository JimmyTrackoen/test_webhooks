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
            regexpFilterExpression: '^(refs/heads/main|refs/heads/developpement)$'
        )
    }
    
    stages {
        stage('run') {
            steps {
                sh 'echo "program is re run update MAJ ONLY IN DEV !!"'
            }
        }
        
        stage('master-branch-stuff'){
            steps {
                echo 'run this stage - ony if the branch = master branch'
            }
        }
        
        stage('run 2'){
            steps {
                sh 'echo Hello : `seq 1 10`'
            }
        }
        
        stage('print branch'){
            steps {
                sh 'echo Branch Finded : $ref'
            }
        }
    }
}
