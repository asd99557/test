pipeline {
    agent {label 'windows'}

      stages {
         stage('Build') {
            steps {
              bat 'mkdir build' // create a new folder 
              bat 'touch build/car.txt' //create an empty file
              bat 'echo "chassis" > build/car.txt' // put chassis inside the file
             }
          }
      }
}
