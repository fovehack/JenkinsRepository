pipeline {
    agent any
    stages {
        stage("Comando de CMD") {
            steps {
                //sh para linux
                bat 'ipconfig /flushdns'
                bat 'git --version'
                bat 'java --version'
            }
        }
    }
}
