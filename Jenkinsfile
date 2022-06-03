pipeline{
    agent any
    
    stages{
        stage('source code'){
            steps{
                git url: 'https://github.com/thiru9880/python-project.git',
                branch: 'master'
            }
        }
        stage("Build"){
            steps{
                sh 'pip install -r requirements.txt'
            }
        }
        stage('test'){
            steps{
                sh 'python3 test_test1.py'
            }
        }
            
        }
    }

    
