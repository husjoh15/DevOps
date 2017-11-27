#!groovy

pipeline {
	agent any
	tools{
	   maven 'devops_maven'
	}
	stages{
		stage('build')  {
			steps{
		   		sh('echo "Hello World"') 
			}
		}		
	}		
}