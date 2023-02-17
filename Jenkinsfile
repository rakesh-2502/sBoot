pipeline {
	agent any
	stages {
	    stage ('clean up') {
	        steps {
	            cleanWs()
	        }
	    }
	    stage ('clone') {
			steps {
				sh 'git clone https://github.com/rakesh-2502/sBoot.git'
			}
		
		}
		stage ('build') {
			steps {
			    dir ('sBoot'){
				    sh 'mvn clean install -DskipTests'
			    }
			}
		
		}
		stage ('test') {
			steps {
			    dir ('sBoot'){
				    sh 'mvn test'
			  
			    }
			  
			}
		
		}
		
	}
}
