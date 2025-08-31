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

        stage('Run Ansible Playbook') {
            steps {
                bat 'ansible-playbook playbook.yml'
            }
        }
    }
}
