
pipeline {
    agent any

    environment {
		JIRA_HOME= 'C:/Atlassian/home'
	    	CATALINA_HOME= 'C:/Atlassian/jira'
	    	JAVA_HOME = 'C:/Program Files/Java/jdk1.8.0_211'
                JRE_HOME = 'C:/Program Files/Java/jdk1.8.0_211/jre'
        }

    stages {
       	stage('jira-installation') {
		steps {
                sh '''
                mkdir C:/Atlassian
                mkdir C:/Atlassian/home
		cp -r C:/shared/jira C:/Atlassian	
                '''
            }
        }
        stage('launch-jira') {
            steps {
                bat 'C:\\Atlassian\\jira\\bin\\start-jira.bat'
            }
		}
	}
}
