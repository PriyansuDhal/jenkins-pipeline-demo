pipeline {
  agent any

  stages {
    stage('Clone Repo') {
      steps {
        git url: 'https://github.com/PriyansuDhal/react_docker_app.git', branch: 'main'
      }
    }

    stage('Build Docker Image') {
      steps {
        sh 'docker build -t react-docker-app .'
      }
    }

    stage('Run Docker Container') {
      steps {
        sh '''
          docker rm -f react-docker-container || true
          docker run -d -p 3000:3000 --name react-docker-container react-docker-app
        '''
      }
    }
  }
}
