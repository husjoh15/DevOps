pipeline {
	agent any
	stages{
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
		
		stage('build image') {
			steps{
				dir('project'){
				  sh('docker build -t <TAG>')
				}
			}
		}
		
			
	}		
}