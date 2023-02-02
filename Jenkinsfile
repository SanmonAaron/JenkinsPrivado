pipeline {
    agent any
    triggers{
        cron('H/5 * * * *')
    }
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
            stage('parallel1') {
                steps {
                    echo "Paralelo 1"
                }
            }
            stage('parallel2') {
                steps {
                    echo "Paralelo 2"
                }
            }
          }
        }
    }
}