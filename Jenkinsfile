pipeline{
        stages{
        stage('clone'){
            steps{
            }
        }
        stage('test') {
    
            steps{
            sh 'echo "test"'
        }
    }
        stage('createfile'){
            steps{
                sh 'touch text-$BUILD_ID'
            }
        }
        }
    }


    