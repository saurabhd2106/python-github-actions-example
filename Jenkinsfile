pipeline {
    agent any

    stages {
        
         stage('Install Dependency') {
            steps {
               
            sh "python -m pip install --upgrade pip"
            sh "pip install -r requirements.txt"
               
            }

            
        }
        
        stage('Build') {
            steps {
                echo "Build"
            }
            
            post {
                always {
                    echo "Post Build"  
                }
                
            }
            
        }
        
       
    }
}
