#!groovy

pipeline {
	agent any
	
	stages{
		stage('build')  {
			steps{
		   		sh('echo "Hello World"') 
			}
			steps{
				tools{
	   				maven 'devops_maven'
				}
			}
		}		
	}		
}