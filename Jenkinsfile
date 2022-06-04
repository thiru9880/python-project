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
                sh 'python3 test_test1.py'
                // junit '**/test-reports/*.xml'
                sh '.py test --verboose --junit-xml test-reports/results.xml sources/test_test1.py'

            }
        }

            
        }
    }

    
