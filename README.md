# Mind Map: Функциональные возможности скоринговой системы

```mermaid
mindmap
  root((Скоринговая система банка))
    Клиентская часть
      Вход в систему
        Регистрация
        Авторизация
      Просмотр рейтинга
        История транзакций
        Анализ платежей
    API
      Авторизация
      Обработка запросов
        Валидация данных
        Логирование
    Сервер
      Алгоритмы скоринга
        Кредитный анализ
        Риски клиента
      Логирование
        Мониторинг
        Хранилище логов
    База данных
      Данные клиентов
      История запросов
      Кэширование результатов
```

# 3. Диаграмму путешествия пользователя (User Journey Diagram)
```mermaid
journey
    title Путь клиента в системе
    section Регистрация
      Клиент: 5: Ввод личных данных
      API: 4: Валидация информации
      Сервер: 4: Сохранение данных
    section Запрос оценки кредита
      Клиент: 5: Оформление запроса
      API: 4: Передача данных
      Сервер: 5: Анализ данных
      База данных: 5: Получение истории
    section Получение результата
      Сервер: 4: Генерация отчета
      API: 4: Отправка данных клиенту
      Клиент: 5: Просмотр результата
```
# 4. Квадрант-граф приоритетов функционала
```mermaid
scatterChart
    title Functional Development Priorities
    x-axis Low Priority --> High Priority
    y-axis Low Complexity --> High Complexity

    point "Risk Analysis" : 9, 9
    point "API Integration" : 8, 8
    point "Scoring Reports" : 7, 9
    point "Error Handling" : 6, 6
    point "Authorization and Security" : 5, 5
    point "Query History" : 4, 8
    point "Support Chat" : 3, 7
    point "Email Notifications" : 2, 3
    point "Recommendations" : 1, 2


```
# 4. Гит граф (Gitgraph)
```mermaid
```mermaid
gitGraph
    commit "Initialization of project"
    branch client
    checkout client
    commit "Development of client interface"
    commit "Adding request handling"
    checkout main
    merge client

    branch server
    checkout server
    commit "API implementation"
    commit "Database connection"
    checkout main
    merge server

    commit "System testing"
    tag "v1.0.0"

    branch improvements
    checkout improvements
    commit "Log improvement"
    checkout main
    merge improvements
    tag "v1.1.0"
```
