pipeline {
	agent none 
	stages {
		stage ('build') {
			agent { label 'slave1' }
			steps {
				sh '''
						echo "this is build stage"
						sleep 2
				   '''	
			} 
		}
		parallel {
		stage ('deploy1') {
			agent { label 'slave1' }
			steps {
				sh '''
						echo "this is deploy stage"
						sleep 2
				   '''	
			}	   
		}
		
		stage ('deploy2') {
			agent { label 'slave1' }
			steps {
				sh '''
						echo "this is deploy stage"
						sleep 2
				   '''	
			}	   
		}
		}
		stage ('test') {
			agent { label 'slave2' }
			steps {
				git 'https://github.com/Gangadhar-s-web/pipeline.git'
				sh '''
						echo "this is test stage"
						sleep 2
				   '''	
			}	   
		}
	}
}
