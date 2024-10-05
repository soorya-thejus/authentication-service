pipeline {
    agent any
    tools {
        maven 'maven'
        jdk 'jdk-17'
    }
    stages {
        stage('Clone') {
            steps {
                git url: 'https://github.com/soorya-thejus/authentication-service.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                bat "mvn clean install -DskipTests"
            }
        }
        stage('Test') {
            steps {
                bat "mvn test"
            }
        }
        stage('Deploy') {
            steps {
<<<<<<< HEAD
		bat "docker rm -f auth-container"
                bat "docker rmi -f auth-image"
=======
                bat "docker rm -f my-auth-container"
                bat "docker rmi -f my-auth-image"
>>>>>>> abd95c89dc0fe0e7ea5b6070ddbd383143bbfb1e
                bat "docker build -t auth-image ."
                bat "docker run -p 8090:8090 -d --name auth-container auth-image"
            }
        }
    }
}
