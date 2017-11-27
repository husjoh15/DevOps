#!groovy

pipeline {
	agent any
	tools{
	   maven 'apache-maven-3.5.2'
	}
	stages{
		stage('build')  {
			steps{
		   		sh('echo "Hello World"') 
			}
		}		
	}		
}