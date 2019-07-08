
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
				unzip //10.87.1.186/apps/Applications/IBM Rational/Jira_Automation/atlassian-jira-software-8.2.1.zip -d C:/Atlassian
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
