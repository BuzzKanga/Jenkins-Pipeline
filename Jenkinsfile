pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                echo 'Fetch the source code from: %DIRECTORY_PATH%'
                echo 'Compile the code and generate any necessary artifacts'
            }
        }
        stage('Test') {
            steps {
                echo 'Unit Test'
                echo 'Integration Test'
            }
        }
        stage('Code Quality Check') {
            steps {
                echo 'Check the quality of the code'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy the application to a testing environment: '
            }
        }
        stage('Approval') {
            steps {
                sleep(10) // wait 10 seconds
                echo 'Approved' 
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Unit Test'
            }
        }
    }
    
}