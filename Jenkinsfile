pipeline {
    agent any 
    stages {
        stage('1. Build') {
            steps {
                echo 'Starting.......'
                echo 'Fetch the source code from: %DIRECTORY_PATH%'
                echo 'Compile the code and package the code using the build automation tool: Maven'
            }
        }
        stage('2. Unit and Integration Tests') {
            steps {
                echo 'Run unit and integration tests to ensure different components work together as expected.'
                echo 'Test automation tool used are: JUnit (for unit tests) and Katalon (for integration test)'
                sleep(2) // wait 2 seconds
                emailext(attachLog: true, body: 'The unit and integration tests have now completed', subject: 'Unit and Integration Testing Status - $BUILD_STATUS', to: 'schristolis@gmail.com')
            }
        }
        stage('3. Code Analysis') {
            steps {
                echo 'Analyse code and check it meets industry standards'
                echo 'SonarQube used to perform code analysis'
            }
        }
        stage('4. Security Scan') {
            steps {
                echo 'Code scanned for vulerabilities using: Nessus'
                sleep(2) // wait 2 seconds
                emailext(attachLog: true, body: 'The security scans have now completed', subject: 'Security Scans Status - $BUILD_STATUS', to: 'schristolis@gmail.com')
            }
        }
        stage('5. Deploy to Staging') {
            steps {
                echo 'Copying code to AWS EC2 staging environment'
                sleep(2) // wait 2 seconds
            }
        }
        stage('6. Integration tests on staging') {
            steps {
                echo 'Run integration tests in satging environment' 
                sleep(2) // wait 2 seconds
            }
        }
        stage('7. Deploy to Production') {
            steps {
                echo 'Copying code to AWS EC2 production environment'
                sleep(2) // wait 2 seconds
            }
        }
    }
    
}
