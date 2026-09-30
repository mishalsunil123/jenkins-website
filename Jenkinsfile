pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/mishalsunil123/jenkins-website.git'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                    sudo /usr/bin/cp index.html /var/www/html/index.html
                '''
            }
        }

        stage('Verify') {
            steps {
                sh '''
                    cat /var/www/html/index.html
                '''
            }
        }
    }
}
