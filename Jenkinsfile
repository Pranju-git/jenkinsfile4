pipeline {
	agent{
	label 'new-slave'
	}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			 sh '/home/admin/appfiles/apache-maven-3.9.6/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			sh 'cp target/jenkinsfile4.war  /home/admin/appfiles/apache-tomcat-9.0.85/webapps'

			}}
}}
