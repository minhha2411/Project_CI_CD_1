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
    // Send mail to specific user if build was fail
    post {
        failure {
            emailText(
                subject: "BUILD FAILED: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
                body: "
                    <p>The build failed in Jenkins!</p>
                    <p>Job: ${env.JOB_NAME}</p>
                    <p>Build Number: ${env.BUILD_NUMBER}</p>
                    <p>Build URL: ${env.BUILD_URL}</p>
                    <p>Failed Stage: ${currentBuild.result}</p>
                    <p>Check the console output at ${env.BUILD_URL}console for more details.</p>
                ",
                to: "${RECIPIENT_EMAIL}",
                mimeType: 'text/html'
            )
        }
    }
}