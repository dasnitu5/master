
pipeline {
    agent any

    environment {
		JIRA_HOME= 'C:/Atlassian/home'
	    	CATALINA_HOME= 'C:/Atlassian/jira'
	    	JAVA_HOME = 'C:/java/jdk1.8'
                JRE_HOME = 'C:/java/jdk1.8/jre'
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
