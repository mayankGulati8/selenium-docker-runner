pipeline{
	agent any
	stages{
		stage("Bring docker up"){
			steps{
				sh "docker-compose up"
			}
		}
		stage("Bring grid down"){
			steps{
				sh "docker-compose down"
			}
		}
	}
}