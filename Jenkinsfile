
pipeline {
    agent any
	environment {
    PATH = "%SystemRoot%/system32"
	PATH = "%M2_HOME%"
  }
    stages {
        stage ('Build Servlet Project') {
            steps {
			
                /*For windows machine */
               bat  'mvn clean package'}

            

            post{
                success{
                    echo 'Now Archiving ....'

                    archiveArtifacts artifacts : '**/*.war'
                }
            }
        }
	
		}
	}