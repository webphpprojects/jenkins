pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'composer install --ignore-platform-reqs -n'
                sh 'bin/console server:run'
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