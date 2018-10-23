pipeline {
    agent any

    }


stages{
        stage('Build'){
            steps {
                sh /scripts/practice.sh
            }
            post {
                success {
                   echo 'awesome'
		}
            }
        }

        stage ('Deployments'){
                stage ('Deploy to Staging'){
                    steps {
			echo 'deploy to staging...'
                }

                stage ("Deploy to Production"){
                    steps {
			echo 'deploy to prod'
                    }
		    post {
 			success {
 		          echo 'awesome'
 			   }
			failed {
			  echo 'awful'	
			}
		    }	
                }
            }
        }
    }
}
