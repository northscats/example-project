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
# 1. Архитектура системы
```mermaid
graph LR
    subgraph Клиентская часть
        Клиент
        Фронтенд
    end
    subgraph Серверная часть
        API
        Сервер
        БазаДанных
        Кэш
    end
    Клиент --> Фронтенд
    Фронтенд --> API
    API --> Сервер
    Сервер --> БазаДанных
    Сервер --> Кэш
    API --> Логи
```
