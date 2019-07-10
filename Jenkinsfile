
pipeline {
    agent any

    environment {
		JIRA_HOME= 'C:/Atlassian/home'
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
