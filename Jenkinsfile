pipeline {
	agent any 
	
       stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/shivani/Documents/devops/apache-maven-3.9.6/bin/mvn install'
		   }}
		stage('Deployment'){
		   steps {
		sh 'cp target/red1.war /home/shivani/Documents/devops/apache-tomcat-9.0.88/webapps'
		   }}	
	       stages {
		       stage {
			       slackSend baseUrl: 'https://hooks.slack.com/services/', channel: 'april-fool', color: 'good', message: 'hello', teamDomain: 'devops', tokenCredentialId: 'april'
}}
