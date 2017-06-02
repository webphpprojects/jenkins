pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'composer install --ignore-platform-reqs -n'
            }
        }
        stage('Tests') {
            steps {
                sh 'vendor/bin/phpcs ./src --standard=PSR2 --extensions=php -n -s'
                sh 'vendor/bin/simple-phpunit'
            }
        }
    }
}