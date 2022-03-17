pipeline {
agent {label 'windows'}
    tools { 
        maven 'Maven' 
    }
    stages {
        stage('Build') {
            steps {
                snDevOpsStep()
                snDevOpsChange()
                bat 'mvn clean install -DskipTests=true'
            }
        }
        stage('Unit Test') {
            steps {
                snDevOpsStep()
                bat "mvn test -Dtest=AppTest"
            }
        }
        stage('Deploy') {
            steps {
                snDevOpsStep()
                snDevOpsChange()
                // bat "mvn -B deploy"
                // bat "mvn -B release:prepare"
                // bat "mvn -B release:perform"
                // deploy using kubernetes - kubectl
                 echo "Deploy to prod"
            }
        }
    }
}
