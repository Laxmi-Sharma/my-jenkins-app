pipeline {
    agent any

    stages {
        stage('clone repo and clean it') {
            steps {
                bat "rm -rf my-jenkins-app"
                bat "git clone https://github.com/Laxmi-Sharma/my-jenkins-app.git"
                bat "mvn clean -f my-jenkins-app"
            }
        }
        stage('Test') {
            steps {
                bat "mvn test -f my-jenkins-app"
            }
        }
        stage('Deploy') {
            steps {
                bat "mvn package -f my-jenkins-app"
            }
        }
    }
}