pipeline{
	agent any
	stages{
		stage("Pull the image"){
			steps{
				sh "docker pull 888777666/selenium-docker"
			}
		}
		stage("Bring grid up"){
			steps{
				sh "docker-compose up -d hub chrome firefox"
			}
		}
		stage("Run Test"){
			steps{
				sh "docker-compose up flightsearch search"
			}
		}
}		
		post{
			always{
				archiveArtifacts artifacts: 'output/**'
				sh "docker-compose down"
			}
		}
	}
