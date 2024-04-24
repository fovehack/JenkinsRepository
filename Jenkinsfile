def diaSemana = Calendar.getInstance().get(Calendar.DAY_OF_WEEK)
def usuario = System.getenv('USER')
def ciudad = "Torre del Mar" // Reemplaza con tu ciudad

pipeline {
    agent any

    stages {
        stage('Calcular operaciones matemáticas (Lunes)') {
            when {
                expression { diaSemana == Calendar.MONDAY }
            }
            steps {
                def num1 = 10
                def num2 = 5

                echo "Suma: ${num1 + num2}"
                echo "Resta: ${num1 - num2}"
                echo "Multiplicación: ${num1 * num2}"
                echo "División: ${num1 / num2}"
            }
        }

        stage('Informar usuario y fecha (Martes)') {
            when {
                expression { diaSemana == Calendar.TUESDAY }
            }
            steps {
                echo "Usuario: ${usuario}"
                echo "Fecha actual: ${new Date()}"
            }
        }

        stage('Mensaje de ejecución (Miércoles)') {
            when {
                expression { diaSemana == Calendar.WEDNESDAY }
            }
            steps {
                echo "Pipeline ejecutado exitosamente."
            }
        }

        stage('Informar clima (Jueves)') {
            when {
                expression { diaSemana == Calendar.THURSDAY }
            }
            steps {
                // Simular consulta del clima (reemplazar con API real)
                def clima = "Soleado con algunas nubes"
                echo "Clima en ${ciudad}: ${clima}"
            }
        }

        stage('Generar Jenkinsfile (Viernes)') {
            when {
                expression { diaSemana == Calendar.FRIDAY }
            }
            steps {
                // Generar Jenkinsfile con mensaje
                writeFile file: 'jenkinsfile-viernes.groovy', content: """
                    pipeline {
                        agent any

                        stages {
                            stage('Mensaje de felicitación') {
                                steps {
                                    echo '¡Lo estás haciendo de maravilla!'
                                }
                            }
                        }
                    }
                """
            }
        }
    }
}

