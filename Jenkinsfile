pipeline {
    agent any
    
    parameters { 
         string(name: 'tomcat_dev', defaultValue: '35.166.210.154', description: 'Staging Server')
         string(name: 'tomcat_prod', defaultValue: '34.209.233.6', description: 'Production Server')
    } 
 
    triggers {
         pollSCM('* * * * *') // Polling Source Control
     }
 
stages{
        stage('Build'){
            steps {
                sh 'scripts/practice.sh'
            }
            post {
                success {
                    echo 'Now Archiving...'
                }
            }
        }
 
        stage ('Deployments'){
            parallel{
                stage ('Deploy to Staging'){
                    steps {
                       echo 'thank'
			}
                }
 
                stage ("Deploy to Production"){
                    steps {
                      echo 'test'
			}
                }
            }
        }
    }
}
