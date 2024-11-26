pipeline{
    agent any

    stages{
        stage('Checkout'){
            steps{
                git branch: 'main', url: "https://github.com/svetlachka/StudentRegistryAppDemo"
            }
        }
        stage('Install Dependances'){
            steps{
                script{
                   
                        bat 'npm install'
                    
                }
            }
            
        }
        stage('Start App and Run Tests'){
        steps{
            script{
                bat 'start /b npm start'
            }
        }
        }
        stage('run Tests'){
        steps{
            script{
                bat 'npm test'
            }
        }
        }
        
    }
    post{
        always{
            echo "CI pipeline completed"
        }
    }
}