pipeline{
	agent any
	stages{
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
		stage("Bring grid down"){
			steps{
				sh "docker-compose down"
			}
		}
	}
}