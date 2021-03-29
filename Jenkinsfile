pipeline {
    agent any

    stages {
        
         stage('Install Dependency') {
            steps {
               
            sh "python3 -m pip install --upgrade pip"
            sh "pip3 install -r requirements.txt"
               
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
