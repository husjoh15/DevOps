#!groovy

pipeline {
	agent any

	stages{
		stage('mvn v') {
			agent{
				label 'slave'
			}
			tools{
				maven "devops_maven"
			}
			steps{
				sh('mvn --version')
			}
		
		}
		stage('build')  {
			steps{
		   		sh('echo "Hello World"') 
			
			}
		
		}		
	}		
}