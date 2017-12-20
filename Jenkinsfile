pipeline {
	agent any
	stages {
	    stage('API Test') {
			steps {
	    		timeout(time: 10, unit:'MINUTES'){
		    		echo "API Test execution"
   				}
	    	}
	    }
    	stage('Performance Test') {
    		steps {
				timeout(time:10, unit:'MINUTES'){
					echo "Performance Test execution"
				}

    		}
    	}
    	stage('Mining') {
    		steps {
    			echo "Mining Both Reports"
    		}
    	}
   }
}
