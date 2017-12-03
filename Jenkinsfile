#!groovy

pipeline {
	agent any

	stages{
		stage('mvn v') {
			tools{
				jdk "devops_jdk"
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