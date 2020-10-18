pipeline {
    agent any
    stages {
        stage('run') {
            steps {
                sh 'echo "program is re run update"'
            }
        }
        
        stage('run 2'){
            steps {
                sh 'echo Hello : `seq 1 10`'
            }
        }
        
        stage('print ref'){
            steps {
                sh 'ref detected: $ref'
            }
        }
    }
}
