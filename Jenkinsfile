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
        	stage('Checkout Stage'){
			steps{
				cleanWs()
				git url: 'https://github.com/bhatgayatri/WebAppPractice.git'
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
	}
}	
