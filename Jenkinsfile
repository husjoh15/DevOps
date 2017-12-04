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
		stage('deploy'){
			steps{
		    		sh('gcloud auth login')
                   		sh('gcloud config set compute/zone {zone}')
                    		sh('gcloud config set project {project}')
                    		sh('gcloud docker -- push <IMAGE>')
                    		sh('gcloud container clusters get-credentials {cluster} --zone {zone} --project  {project}')
                    		sh('kubectl run project --image=<IMAGE>')
			}
		}
		stage('clean')  {
			tools{
				jdk "jdk"
				maven "maven"
			}
			steps{
				sh('mvn clean')
			}
		}	
	}		
}