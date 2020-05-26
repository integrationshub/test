pipeline {
	agent any
	
	tools {
        maven 'my_local_maven'
    }
	
	stages {
		
		stage('build my application') {
		
			steps {
				//bat 'mvn clean package'
				sh 'mvn clean package'
			}
		
		}
		
		stage('Test my application') {
		
			steps {
				sh 'mvn test'
			
			}
		
		}
		
		stage('deploy my application to cloudHub') {
			
			steps {
				sh 'mvn package deploy -DmuleDeploy'
			
			}
		
		}
		
		
		
	}
}