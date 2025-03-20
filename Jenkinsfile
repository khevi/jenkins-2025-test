pipeline {
    agent any
        stages{
            stage('Clone'){
                steps{
                    sh 'echo "clone"'
                }
            }
            stage('test'){
                steps{
                    sh 'echo "test"'
                }
            }
            stage ('Createfile'){
                steps{
                    sh 'touch text-$BUILD_ID'
                }
            }
        }
       
}

    