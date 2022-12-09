pipeline {
    agent any

 

    stages {
        stage('git repo and clean') {
            steps {
                bat  "rmdir /s /q   customer"
                bat "git clone https://github.com/krish-220/Online-Booking-Carpenter.git"
                bat "mvn clean -f customer"
            }
        }
        stage('install') {
            steps {
                bat  "mvn install -f customer"
            }
        }
        stage('test') {
            steps {
                bat  "mvn test -f customer"
            }
        }
        stage('package') {
            steps {
            bat "mvn package -f customer"

            }
        }
    }
}
