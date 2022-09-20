pipeline {
    agent any
environment {
	   checkoutCode = true
	   runSonarScan = true
	   deployNexusArtifact = true
}
    stages {
        stage('Build') {
		
            steps {
                echo 'Building...'
            }
        }
   
        stage('Deploy') {
		when { expression { "${checkoutCode}" == 'true' } }
            steps {
                echo 'Deploying...'
            }
        }
        
        stage('Testing') {
            steps {
                echo 'Testing...'
            }
        
    }
     
        stage('Maintaince') {
		when { expression { "${runSonarScan}" == 'true' } }
            steps {
                echo 'Maintaince...'
            }
        }
	    
	 stage('Release') {
		 when { expression { "${runSonarScan}" == 'false' } }
            steps {
                echo 'Releasing...'
            }
        }
	    
	}
   
}
