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
                bat 'npm start &'
                bat 'wait-on http://localhost:8090'
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