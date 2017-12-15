pipeline {
	agent any
	stages {
    	stage('Compile') {
    		timeout(1){
	    		steps {
	    			sh "./task.sh"
	    			echo "mvn clean compile"
	    			echo "Build Quality mining"
	    		}
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
    			echo "mvn package"
    			echo "Promoting package"
    		}
    	}
   }
}
