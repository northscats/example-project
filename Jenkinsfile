pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Шаг проверки кода из репозитория
                git url: 'https://github.com/northscats/example-project.git', branch: 'main', credentialsId: 'github-credentials'
            }
        }
        
        stage('Build') {
            steps {
                // Шаг сборки
                echo 'Building the project...'
                // Пример: Выполнение команды сборки (для Maven проекта)
                // sh 'mvn clean install'
            }
        }
        
        stage('Test') {
            steps {
                // Шаг тестирования
                echo 'Running tests...'
                // Пример: запуск тестов
                // sh 'mvn test'
            }
        }
        
        stage('Deploy') {
            steps {
                // Шаг развертывания
                echo 'Deploying the application...'
                // Пример: деплой на сервер
                // sh 'scp target/*.jar user@server:/path/to/deploy'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
