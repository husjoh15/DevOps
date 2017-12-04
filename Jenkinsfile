#!groovy

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
                   		sh('gcloud config set compute/zone europe-west3-a')
                    		sh('gcloud config set project westerdals-185117')
                    		sh('gcloud docker -- push <IMAGE>')
                    		sh('gcloud container clusters get-credentials westerdals-k8s2-cluster --zone europe-west3-a --project  westerdals 185117')
                    		sh('kubectl run project --image=<IMAGE>')
			}
		}
		stage('clean')
			tools{
				jdk "jdk"
				maven "maven"
			}
			steps{
				sh('mvn clean')
			}	
	}		
}