pipeline {
    agent any 
    environment {
        RECIPIENT_EMAIL = 'hoangminhha2411@gmail.com'
    }
    stages {
        stage('Build') {
            steps {
                echo "Start building stage ...."
                echo "Test loggout credential ...."
                echo "In dev enviroment"
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