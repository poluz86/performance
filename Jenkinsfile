pipeline {
	agent any
	stages {
		stage('Checkout') {
			steps {
				echo "Hello!"
         	}
	}
    	stage('Compile') {
    		steps {
    			echo "mvn clean compile"
    			echo "Build Quality mining"
    		}
    	}
    	stage('Unit Test') {
    		steps {
    			echo "mvn clean test"
    			echo "junit report.xml"
    		}
    	}
    	stage('SonarQube') {
    		steps {
    			echo "sonar projectKey"
    			echo "Cyclomatic Complexity mining"
    			echo "Technical Debt mining"
    		}
    	}
    	stage('Promote') {
    		steps {
    			echo "Promoting package"
    		}
    	}
   }
}
