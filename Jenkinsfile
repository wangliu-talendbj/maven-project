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
			parallel{
				stage('p1'){
					echo 'hello'
				}
				stage('p2'){
					echo 'yes'
				}
			}
		}
	}
}
