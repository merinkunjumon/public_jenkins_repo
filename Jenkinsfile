pipeline {
    agent any
    tools {
        maven 'm86'
        jdk 'jdk8'
    }
    stages {
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
       /* stage('Test') {
           steps {
               sh 'mvn test'
           }
        } */
    }
    post {
        success {
            slackSend channel: 'merinkunjumon95', message: "Build for project ${BUILD_NUMBER} is sucessfull"
        }
        }
}

    