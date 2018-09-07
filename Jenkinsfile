#!groovy

node {
	   
	stage('Checkout'){

          checkout scm
       }

       stage('BuildArtifact and sending to nexus'){

         // sh 'mvn install'
	       
	       //sh 'mvn clean'
	       bat 'mvn clean deploy'
       }
	   
      stage('Sonar') {
                    //add stage sonar
                   // sh 'mvn sonar:sonar'
	      bat 'mvn sonar:sonar'
                }
	stage('Tomcat') {
		copy %WORKSPACE%\target\maven-web-project-1.3.war C:\Devopssoft\apache-tomcat-9.0.8\webapps\
	}
       
}
