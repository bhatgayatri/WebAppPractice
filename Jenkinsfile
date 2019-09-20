pipeline{
	tools{
		maven 'M2_HOME'
		jdk 'JAVA_HOME'
	}
	agent {
    		node {
			label ''
    		}
  	}
	stages{
<<<<<<< HEAD
           stage('Checkout Stage'){
		   steps{
			   cleanWs()
                  git url: 'https://github.com/bhatgayatri/my-app.git'
			   bat 'mvn validate'
                 bat 'mvn clean'
		      
	       	}
          	}
	
    
	  stage('Compile Stage'){
	       steps{
		       bat 'mvn compile'
		       bat 'mvn test-compile'
	       }
             }
		stage('self phase'){
	       steps{
		       bat 'mvn process-test-resources'
	       }
             }
		
          stage('Static Code Analysis Stage'){
	        steps{
	         	bat 'mvn sonar:sonar -Dsonar.host.url=http://localhost:9000/sonar/'
		     }
	 	}
	  stage('Testing Stage'){
	        steps{
		  		bat 'mvn test'
				bat 'mvn surefire:test'
	     	  	        junit 'target/surefire-reports/*.xml'
			      
	      	             }
=======
        	stage('Checkout Stage'){
			steps{
				cleanWs()
				git url: 'https://github.com/bhatgayatri/WebAppPractice.git'
				bat 'mvn validate'
				bat 'mvn clean'
>>>>>>> e58b1aa7c532f8f6569845f658415500f4209bba
			}
        	}
	   	stage('Compile Stage'){
			steps{
				bat 'mvn compile'
				bat 'mvn test-compile'
			}
        	}
	}
}	
