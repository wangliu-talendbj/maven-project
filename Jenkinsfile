pipeline {
	agent any
	
	stages{
		stage('initial'){
			steps{
				echo 'I'm starving'
			}
		}
		stage('next'){
			steps{
				sh 'scripts/practice.sh'
			}
			post{
				success{
					echo 'awesome'
				}
				failed{
					echo 'awful'
				}
			}
		}
		stage('finally'){
			steps{
				echo 'well done'
			}
		}
	}
}
