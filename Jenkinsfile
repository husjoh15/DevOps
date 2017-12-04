#!groovy

pipeline {
	agent any

	stages{
		stage('mvn clean') {
			tools{
				jdk "devops_jdk"
				maven "devops_maven"
			}
			steps{
				sh('mvn clean')
			}
		
		}
		stage('mvn install')  {
			tools{
				jdk "devops_jdk"
				maven "devops_maven"
			}
			steps{
		   		sh('mvn install') 
			}
		
		}		
	}		
}