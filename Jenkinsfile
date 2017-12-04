#!groovy

pipeline {
	agent {
		docker { image '3.5.2-jdk-8' }
	}

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