   pipeline{
	agent any
	stage{
		stage("Build){
			step{
				sh 'mvn install'
		
			}
		}
		stage("Build The Docker Image" ){
			step{
				sh 'docker build -t sreeni15/jenkinsproject-spring-app:v1.1 . && docker images'
		
				} 
			stage("Push The Docker Image" ){
			step{
				sh 'docker push sreeni15/jenkinsproject-spring-app:v1.1 .'
				sh 'docker images'
		
				}
			
			}
		}
	}
}
