pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
    
    parallel firstBranch: {
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
        }, secondBranch: {
        stage('Testing') {
            steps {
                echo 'Testing...'
            }
        }
    }
     
        stage('Maintaince') {
            steps {
                echo 'Maintaince...'
            }
        }
	    
	 stage('Release') {
            steps {
                echo 'Releasing...'
            }
        }
	    
	}
   
}
