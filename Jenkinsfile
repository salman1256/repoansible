pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/salman1256/repoansible.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t my-app:latest ./app'
            }
        }

        stage('Run Container') {
    steps {
        bat 'docker run -d -p 8080:80 --name myapp my-app:latest'
        }
        }

    }
}
