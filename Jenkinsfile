pipeline {
    agent any
    parameters {
        string(name: 'persona_a_saludar', defaultValue: 'Aarón', description: 'A quién debería saludar?')
    }

    stages {

        stage('execution') {
            steps {
                sh "node saludo.js ${params.persona_a_saludar}"
            }
        }
        stage('parallel') {
            parallel {
            stage('execution') {
                steps {
                    echo 'Paralelo 1'
                }
            }
            stage('execution') {
                steps {
                    echo 'Paralelo 2'
                }
            }
          }
        }
    }
}