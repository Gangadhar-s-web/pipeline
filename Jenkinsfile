pipeline {
	agent any 
	stages {
		stage ('build') {
			steps {
				sh '''
						echo "this is build stage"
						sleep 2
				   '''	
			} 
		}
		
		stage ('deploy') {
			steps {
				sh '''
						echo "this is deploy stage"
						sleep 2
				   '''	
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
		}
		stage ('test') {
			steps {
				sh '''
						echo "this is test stage"
						sleep 2
				   '''	
			}	   
		}
	}
}
