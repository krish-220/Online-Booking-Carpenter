pipeline{
	agent any
	stages{
	
	steps{
	stage('Compile Stage'){
		withMaven(maven : 'maven_3_8_6') {
			sh 'mvn clean compile'
			}
		}
	}
	
	stage('Testing Stage'){
		withMaven(maven : 'maven_3_8_6') {
			sh 'mvn test'
			}
		}
		
	stage('Deployment Stage'){
		withMaven(maven : 'maven_3_8_6') {
			sh 'mvn deploy test'
			}
		}	
		
	}
	
	}
	
