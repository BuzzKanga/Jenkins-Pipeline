pipeline {
    agent any 
    stages {
        stage('1. Build') {
            steps {
                echo 'Fetch the source code from: %DIRECTORY_PATH%'
                echo 'Compile the code and generate any necessary artifacts'
            }
        }
        stage('2. Test') {
            steps {
                echo 'Unit Test'
                echo 'Integration Test'
            }
        }
        stage('3. Code Quality Check') {
            steps {
                echo 'Check the quality of the code'
            }
        }
        stage('4. Deploy') {
            steps {
                echo 'Deploy the application to a testing environment: '
            }
        }
        stage('5. Approval') {
            steps {
                sleep(3) // wait 3 seconds
                echo 'Approved' 
            }
        }
        stage('6. Deploy to Production') {
            steps {
                echo 'Unit Test'
            }
        }
    }
    
}