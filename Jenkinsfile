pipeline{

        environment {
          registry = "matanbedani/docker-test"
          registryCredential = ‘dockerid’
  }

	agent any

		stage('Pull') {

			steps {
				sh 'docker pull nginx:latest'
			}
		}

		stage('Pull') {

			steps {
				sh 'docker build -t nginx:latest1'
			}
		}
				
		stage('Push') {

			steps {
				sh 'docker push nginx:latest'
			}
		}
	}

	post {
		always {
			sh 'docker logout'
		}
	}

}
