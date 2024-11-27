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
quadrantChart
    title Functional Development Priorities
    x-axis Priority
    y-axis Complexity
    "Implement Immediately": [ ["Risk Analysis", 85, 95], ["API Integration", 75, 85], ["Scoring Reports", 70, 90] ]
    "Needs Thorough Analysis": [ ["Error Handling", 65, 60], ["Authorization and Security", 55, 50] ]
    "Plan for Near Future": [ ["Query History", 45, 80], ["Support Chat", 40, 75] ]
    "Might Be Dropped": [ ["Email Notifications", 20, 30], ["Recommendations", 15, 25] ]

```
# 4. Гит граф (Gitgraph)
```mermaid
gitGraph
    commit id: "Инициализация проекта"
    branch клиент
    checkout клиент
    commit id: "Разработка клиентского интерфейса"
    commit id: "Добавление обработки запросов"
    checkout main
    merge клиент id: "Интеграция клиента"

    branch сервер
    checkout сервер
    commit id: "Реализация API"
    commit id: "Подключение базы данных"
    checkout main
    merge сервер id: "Интеграция сервера"

    commit id: "Тестирование системы"
    tag "v1.0.0" 

    branch улучшения
    checkout улучшения
    commit id: "Улучшение логирования"
    checkout main
    merge улучшения id: "Релиз v1.1"
    tag "v1.1.0"


```
