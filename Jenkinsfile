pipeline {
	agent any
	
	stages{
		stage('initial'){
			steps{
				echo 'Im starving'
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
