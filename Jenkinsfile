pipeline {
    agent any
        stages{
            stage('codescan'){
                steps{
                    sh 'trivy fs . -o result.html'
                    sh 'cat result.html'
                    }
            }
            stage('dockerLogin'){
                steps{
                    sh 'aws ecr get-login-password --region us-east-1 | \
                    docker login --username AWS --password-stdin 585008070473.dkr.ecr.us-east-1.amazonaws.com'
                }
                
            }
            stage('dockerImageBuild'){
                steps{
                    sh 'docker build -t'
                }
            }
            stage('dockerImageTag'){
                steps{
                    sh 'docker tag jenkins-new-ci:latest 585008070473.dkr.ecr.us-east-1.amazonaws.com/jenkins-new-ci:latest'
                }
            }
            stage('pushImage'){
                steps{
                    sh 'docker push 585008070473.dkr.ecr.us-east-1.amazonaws.com/jenkins-new-ci:latest'
                }
            }
        }
       
}

    