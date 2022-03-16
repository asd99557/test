pipeline {
    agent {label 'windows'}

   stages ('Build') {
      steps {
          sh 'mkdir build' // create a new folder 
          sh 'touch build/car.txt' //create an empty file
          sh 'echo "chassis" > build/car.txt' // put chassis inside the file
  }
}
   stages ('Test') {
      steps {
          sh 'test -f build/car.txt'
          sh 'grep "chassis" build/car.txt' 
    } 
}
  stages ('Publish') {
     steps {
     archiveArtifacts artifacts: 'build/'  
    }
}
}
