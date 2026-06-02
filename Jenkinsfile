
pipeline {
    agent any

    stages {

        stage('Checkout Repository') {
            steps {
                git branch: 'master', url: 'https://github.com/Alekhyaareddy/etp'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t newone .'
            }
        }
        stage('Run Container') {
            steps {
                bat 'docker run -d -p 8087:80 newone'
            }
        }

       

      

    }
}