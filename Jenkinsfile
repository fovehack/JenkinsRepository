pipeline {
    agent any

    stages {
        stage('Ejecutar acciones según el día de la semana') {
            steps {
                def diaActual = calendario.get(Calendar.DAY_OF_WEEK)

                if (diaActual == Calendar.SUNDAY) {
                    // Calcular operaciones matemáticas (Lunes)
                    def num1 = 10
                    def num2 = 5
                    echo "Suma: ${num1 + num2}"
                    echo "Resta: ${num1 - num2}"
                    echo "Multiplicación: ${num1 * num2}"
                    echo "División: ${num1 / num2}"
                } else if (diaActual == Calendar.MONDAY) {
                    // Informar usuario y fecha (Martes)
                    def usuario = System.getenv('USER')
                    echo "Usuario: ${usuario}"
                    echo "Fecha actual: ${new Date()}"
                } else if (diaActual == Calendar.TUESDAY) {
                    // Mensaje de ejecución (Miércoles)
                    echo "Pipeline ejecutado exitosamente."
                } else if (diaActual == Calendar.WEDNESDAY) {
                    // Informar clima (Jueves)
                    // Simular consulta del clima (reemplazar con API real)
                    def clima = "Soleado con algunas nubes"
                    echo "Clima en ${ciudad}: ${clima}"
                } else if (diaActual == Calendar.THURSDAY) {
                    // Generar Jenkinsfile (Viernes)
                    writeFile file: 'jenkinsfile-viernes.groovy', text: """
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
                } else {
                    // Manejar día no válido (Sábado)
                    echo "Día de la semana no válido: ${diaActual}"
                }
            }
        }
    }
}
