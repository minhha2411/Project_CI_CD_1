pipeline {
    agent any 
    environment {
        RECIPIENT_EMAIL = 'hoangminhha2411@gmail.com'
    }
    stages {
        stage('Build') {
            environment {
                USER_NAME = credentials('e9ab3c86-b7d8-4311-ad35-91e6a6fac383')
            }
            steps {
                echo "Start building stage ...."
                echo "Test loggout credential ...."
            }
        }
        stage('Test') {
            steps {
                echo "Start testing stage ...."
            }
        }
        stage('Deploy') {
            steps {
                echo "Start deploy stage ...."
            }
        }
    }
}