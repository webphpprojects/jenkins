pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'composer install --ignore-platform-reqs -n'
                bat 'vendor\\bin\\phpcbf.bat .\\src --standard=PSR2 --extensions=php -n -s'
            }
        }
        stage('Tests') {
            steps {
                bat 'vendor\\bin\\phpcs.bat .\\src --standard=PSR2 --extensions=php -n -s'
            }
        }
    }
}