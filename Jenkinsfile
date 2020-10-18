pipeline {
    agent any
    stages {
        stage('run') {
            steps {
                sh 'echo "program is re run update"'
            }
        }
        
        stage('master-branch-stuff'){
            agent any
            when{
                branch 'refs/heads/main'
            }
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
