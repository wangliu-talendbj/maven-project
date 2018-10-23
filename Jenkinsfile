pipeline {
    agent any

stages{
        stage('Build'){
            steps {
                sh '/scripts/practice.sh'
            }
            post {
                success {
                   echo 'awesome'
		}
            }
        }

        stage ('Deployments'){
	    parallel{
                stage ('Deploy to Staging'){
                    steps {
			echo 'deploy to staging...'
                }

                stage ("Deploy to Production"){
                    steps {
			echo 'deploy to prod'
                    }
                }
            }
        }
    } 
  }
}
