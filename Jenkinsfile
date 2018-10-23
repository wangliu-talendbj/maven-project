pipeline {
	agent any
	
	stages{
		stage('initial'){
			steps{
				echo 'I am starving'
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
				failure{
					echo 'awful'
				}
			}
		}
		stage('finally'){
			parallel{
				stage('p1'){
					steps{
						echo 'hello'
					}
				}
				stage('p2'){
					steps{
						echo 'yes'
					}
				}
			}
		}
	}
}

