pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building the CI/CD demo application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Validating the application...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'

                bat '''
                    if not exist "C:\\Deployments\\CICDWebApp" mkdir "C:\\Deployments\\CICDWebApp"
                    copy /Y index.html "C:\\Deployments\\CICDWebApp\\index.html"
                '''
            }
        }
    }
}
