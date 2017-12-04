#!groovy

pipeline {
	agent any

	stages{
		stage('test')
		{
			tools{
				jdk "jdk"
				maven "maven"
			}
			steps{
				sh 'mvn --version'
			}
		}
		stage('mvn clean') {
			tools{
				jdk "jdk"
				maven "maven"
			}
			steps{
				sh('mvn clean')
			}
		
		}
		stage('mvn install')  {
			tools{
				jdk "jdk"
				maven "maven"
			}
			steps{
		   		sh('mvn install') 
			}
		
		}	
			
	}		
}