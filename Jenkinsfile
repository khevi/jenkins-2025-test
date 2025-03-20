pipeline {
    agent any
        stages{
            stage('Clone'){
                steps{
                    sh 'echo "clone"'
                    sh 'uname -r'
                    sh 'uname -a'
                                    }
            }
            stage('test'){
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

    