pipeline {
  agent any

  environment {
    IMAGE_NAME = "my-ci-cd-app"
    CONTAINER_NAME = "my-container"
  }

  stages {

    stage('Build App') {
      steps {
        sh 'npm install'
      }
    }

    stage('Run Tests') {
      steps {
        sh 'echo "No tests yet"'
      }
    }

    stage('Build Docker Image') {
      steps {
        sh 'docker build -t $IMAGE_NAME .'
      }
    }

    stage('Run Container') {
      steps {
        sh '''
          docker rm -f $CONTAINER_NAME || true
          docker run -d -p 8081:8080 --name $CONTAINER_NAME $IMAGE_NAME
        '''
      }
    }
  }
}