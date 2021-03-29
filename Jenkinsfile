pipeline {
    agent any

    stages {
        
         stage('Install Dependency') {
            steps {
               
            sh "python3 -m pip install --upgrade pip"
            sh "pip3 install -r requirements.txt"
               
            }

            
        }
        
        stage('Quality Scans') {
            steps {
                sh "pip3 install flake8"
                sh "flake8 . --count --select=E9,F63,F7,F82 --show-source --statistics"
                sh "flake8 . --count --exit-zero --max-complexity=10 --max-line-length=127 --statistics"
            }
            
        }

        stage('Tests') {
            steps {
                
                sh "pip3 install pytest"

                sh "export PYTHONPATH=src"

                sh """
                    cd tests;
                    pytest
                """
            }
            
        }
        
       
    }
}
