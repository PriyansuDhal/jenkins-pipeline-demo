pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/PriyansuDhal/react_docker_app.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t react-docker-app .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 3100:3000 react-docker-app'
            }
        }
    }
}
