pipeline {
    agent any
        stages{
            stage('code scan'){
                steps{
                    sh 'trivy fs . -o result.html'
                    
                    }
            }
            stage('dockerImageBuild'){
                steps{
                    sh 'docker -v'
                }
            }
            stage('pushImage'){
                steps{
                    sh 'docker ps'
                }
            }
        }
       
}

    