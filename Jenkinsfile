
pipeline {
    agent any

    stages {
        stage ('Build Servlet Project') {
            steps {
			echo 'Now Archiving ....'
                /*For windows machine 
               bat  'mvn clean package'*/
			   }

            

            post{
                success{
                    echo 'Now Archiving ....'

                    archiveArtifacts artifacts : '**/*.war'
                }
            }
        }
	
		}
	}