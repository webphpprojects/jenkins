pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'composer install --ignore-platform-reqs -n'
            }
        }
        stage('Tests') {
            steps {
                bat 'vendor\\bin\\simple-phpunit.bat'
            }
        }
    }
}