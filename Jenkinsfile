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
                 bat 'cd C:/agent/workspace/test_main/build/car.txt' 
                 bat 'more car.txt' 
              }
          }     
  }  
}    
 
