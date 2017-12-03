#!groovy

pipeline {
	agent any

	stages{
		stage('mvn clean') {
			agent{
				label 'slave'
			}
			tools{
				jdk "devops_jdk"
				maven "devops_maven"
			}
		
		}
		stage('build')  {
			steps{
		   		sh('echo "Hello World"') 
				sh('mvn --version')
			}
		
		}		
	}		
}