pipeline {
    agent any
    stages {
        stage ('Initialize') {
            steps {
               bat 'Build servlet project'
			
            }

            
        }

        post {
		success
            {
            
            			echo 'Deployement Failure on PRODUCTION'
                   archiveArtifacts artifact : '**/*.war'
			}
        }

        
    }
}
