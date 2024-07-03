pipeline {
    agent any
	
	environment {
        registry = ""
        registryCredential = ''
        cartRegistry = ""
    }
	
	stages {
	
	  stage('Build Image') {
	     steps {
		   
		     script {
                dockerImage = docker.build( registry + ":$BUILD_NUMBER", "./javaapi/")
             }

		 }
	  
	  }
	  
	  stage('Deploy Image') {
          steps{
            script {
              docker.withRegistry( cartRegistry, registryCredential ) {
                dockerImage.push("$BUILD_NUMBER")
                dockerImage.push('latest')
              }
            }
          }
	   }

       