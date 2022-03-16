pipeline {
    agent {label 'windows'}

      stages {
         stage('Build') {
            steps {
              sh 'mkdir build' // create a new folder 
              sh 'touch build/car.txt' //create an empty file
              sh 'echo "chassis" > build/car.txt' // put chassis inside the file
             }
          }
      }
}
