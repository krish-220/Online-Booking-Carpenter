pipeline {
    agent any

 

    stages {
        stage('git repo and clean') {
            steps {
                bat  "rmdir /s /q   AwsTwoWheeler"
                bat "git clone https://github.com/Sarathkumara2000/AwsTwoWheeler.git"
                bat "mvn clean -f AwsTwoWheeler"
            }
        }
        stage('install') {
            steps {
                bat  "mvn install -f AwsTwoWheeler"
            }
        }
        stage('test') {
            steps {
                bat  "mvn test -f AwsTwoWheeler"
            }
        }
        stage('package') {
            steps {
            bat "mvn package -f AwsTwoWheeler"

            }
        }
    }
}
