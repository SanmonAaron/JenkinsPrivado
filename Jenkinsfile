pipeline {
    agent any
    parameters {
        string(name: 'persona_a_saludar', defaultValue: 'Aarón', description: 'A quién debería saludar?')
    }

    stages {

        stage('execution') {
            steps {
                sh 'node saludo.js ${persona_a_saludar}'
            }
        }
    }
}