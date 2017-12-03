#!groovy

pipeline {
	agent any

	stages{
		stage('mvn clean') {
			agent{
				label 'slave'
			}
			tools{
				jdk "JDK 8"
				maven "apache-maven-3-5-2"
			}
			steps{
				sh('mvn clean')
			}

		stage('build')  {
			steps{
		   		sh('echo "Hello World"') 
				sh('mvn --version')
			}
		
		}		
	}		
}