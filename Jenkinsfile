pipeline {
    agent any
    
    stages {
        stage('Monday') {
            when {
                expression { return env.BUILD_ID && env.BUILD_ID.startsWith('1') }
            }
            steps {
                script {
                    def num1 = 10
                    def num2 = 5
                    echo "Suma: ${num1 + num2}"
                    echo "Resta: ${num1 - num2}"
                    echo "Multiplicación: ${num1 * num2}"
                    echo "División: ${num1 / num2}"
                }
            }
        }
        
        stage('Tuesday') {
            when {
                expression { return env.BUILD_ID && env.BUILD_ID.startsWith('2') }
            }
            steps {
                script {
                    def user = sh(script: 'whoami', returnStdout: true).trim()
                    def date = sh(script: 'date', returnStdout: true).trim()
                    echo "Usuario que realizó la ejecución: $user"
                    echo "Fecha actual: $date"
                }
            }
        }
        
        stage('Wednesday') {
            when {
                expression { return env.BUILD_ID && env.BUILD_ID.startsWith('3') }
            }
            steps {
                echo "El pipeline se ejecutó correctamente el miércoles."
            }
        }
        
        stage('Thursday') {
            when {
                expression { return env.BUILD_ID && env.BUILD_ID.startsWith('4') }
            }
            steps {
                script {
                    // Aquí puedes incluir código para obtener el clima de tu ciudad y mostrarlo en la consola
                    echo "¡Jueves! Información del clima para tu ciudad."
                    // Ejemplo: 
                    // def weather = sh(script: 'curl http://wttr.in/YourCity?format="%C+%t"', returnStdout: true).trim()
                    // echo "Clima actual: $weather"
                }
            }
        }
        
        stage('Friday') {
            when {
                expression { return env.BUILD_ID && env.BUILD_ID.startsWith('5') }
            }
            steps {
                script {
                    // Aquí generamos un nuevo Jenkinsfile utilizando Groovy
                    writeFile file: 'NuevoJenkinsfile.groovy', text: 'pipeline { \n    agent any \n    stages { \n        stage(\'FridayMessage\') { \n            steps { \n                echo "¡Lo estás haciendo de maravilla!" \n            } \n        } \n    } \n}'
                    echo "Se generó un nuevo Jenkinsfile para el próximo viernes."
                }
            }
        }
    }
}
