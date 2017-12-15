pipeline {
	agent any
	stages {
		try {
	    	stage('Compile') {
	    		steps {
	    			timeout(time:1, unit:'MINUTES'){
	    				sh "./task.sh"
	    				echo "mvn clean compile"
	    				echo "Build Quality mining"
	    			}

	    		}
	    	}
		}
		catch (Exception){
			currentBuild.result = 'UNSTABLE'
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
