pipeline {
   agent { label 'master' }
   stages {
       stage('write') {
           steps {
               script {
               bat 'mkdir build' // create a new folder 
               bat 'type NUL >  build/car.txt' //create an empty file
               bat 'echo "chassis" > build/car.txt' // put chassis inside the file   
               }
           }
       }
       stage('read') {
           steps {
               script {
                   def data = readFile(file: 'build/car.txt')
                   println(data)
               }
           }
       }
   }
}
