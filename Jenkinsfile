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
       
}
