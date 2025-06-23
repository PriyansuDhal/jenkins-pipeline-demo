pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/PriyansuDhal/jenkins-pipeline-demo.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t react-docker-app .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 3000:3000 react-docker-app'
            }
        }
    }
}
