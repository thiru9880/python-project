pipeline{
    agent {
        label "nodejs"
    }
    
    stages{
        stage('source code'){
            steps{
                git url: 'https://github.com/thiru9880/python-project.git',
                branch: 'master'
            }
        }
        stage("Build"){
            steps{
                sh 'pip3 install -r requirements.txt'
            }
        }
        stage('test'){
            steps{
                sh 'pip install -U pytest'
                sh 'python3 test_test1.py'
                // junit '**/test-reports/*.xml'
                sh 'pytest --doctest-modules --junitxml=junit/test-results.xml --cov=. --cov-report=xml'

            }
        }

            
        }
    }

    
