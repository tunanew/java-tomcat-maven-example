
pipeline {
    agent any
    stages {
        stage ('Build Servlet Project') {
            steps {
			path %M2_HOME%
                /*For windows machine */
               bat  'mvn clean package'

                /*For Mac & Linux machine */
               // sh  'mvn clean package'
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