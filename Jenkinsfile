pipeline{
	agent any

	environment{
		PATH = "Program Files/apache-maven/bin:$PATH"
	}

	stages {
		stage("Git Checkout"){
			steps{
				git credentialsId: 'github', url: 'https://github.com/andrestwm/WebApp'
			}
		}

		stage("Maven Build"){
			steps{
				sh "mvn clean package"
			}
		}
	}
}
