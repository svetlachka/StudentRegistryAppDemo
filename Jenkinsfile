pipeline{
    agent any

    environment{
        NODE_VERSIONS = '20.x'
    }
    tools{

        nodejs "${NODE_VERSIONS}"
    }
    stages{
        stage('Checkout'){
            steps{
                checkout scm
            }
        }
        stage('Install Dependances'){
            steps{
                script{
                    if(isUnix()){
                        sh 'npm install'
                    }
                    else{
                        sh 'npm install'
                    }
                }
            }
        }
    }
}