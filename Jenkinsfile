pipeline {
    agent {label 'windows'}

      stages {
         stage('Build') {
            steps {
              bat 'mkdir build' // create a new folder 
              bat 'type NUL >  build/car.txt' //create an empty file
              bat 'echo "chassis" > build/car.txt' // put chassis inside the file 
         }
     }         
         stage('Test') {
            steps {
		     script {
                 Boolean bool = fileExists 'build/car.txt'
                 if (bool) {
                     println "The File exists :)"
                } else {
                     println "The File does not exist :("
				}   
         stage('publish') {
            steps {
		    script {   
                 bat archiveArtifacts artifacts: 'build/'
		    }
      				}
  			} 			     
                  }         
             } 
        }
  }         
}
