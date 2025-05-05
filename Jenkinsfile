pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/suSha4nt/flask-hello-world.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("flask-hello-world-app")
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    docker.run("flask-hello-world-app")
                }
            }
        }
    }
}
