pipeline {
    agent {label 'windows'}
 tools {
     //// Install the Maven version configured.
        Maven 'maven'
    }    
   stages {
       stage('Build') {
            steps {
                echo "Building . .!"
                 bat "mvn -DskipTests clean install"
        }
      }
	    stage('Test') {
		    steps {
			    echo 'Testing..'
				bat "mvn -DskipTests test"
				
			}		
        }
		stage('Deploy') {
		    steps {
				echo 'Deploying...'
			}
		}
	}
}	
