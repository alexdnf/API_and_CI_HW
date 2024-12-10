pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Запускаем Java-приложение в фоновом режиме
                bat 'java -jar ./artifacts/app-mbank.jar &'

                // Устанавливаем права на выполнение для скрипта Gradle
                bat 'chmod +x gradlew'

                // Запускаем тесты с выводом информации
                bat './gradlew test --info'
            }
        }
    }
}
