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
                bat 'vendor\\bin\\phpcs.bat .\\src --standard=PSR2 --extensions=php -n -s'
            }
        }
    }
}