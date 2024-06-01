## SentinelGuard - это проект, предназначенный для обеспечения безопасного и эффективного управления клиентскими и мошенническими данными с использованием микросервисной архитектуры. Основные компоненты проекта включают в себя:

## Технологии
- Java
- Spring Boot
- Kafka
- PostgreSQL
- Docker
- Zipkin
- Liquibase
- Sleuth
- Eureka

1. Балансировщик нагрузки: Обеспечивает равномерное распределение входящих запросов между микросервисами для повышения отказоустойчивости и производительности.
2. Микросервис "Fraud": Отвечает за обработку данных, связанных с мошенничеством. Хранит данные в базе данных MongoDB и взаимодействует с Kafka для асинхронной отправки уведомлений.
3. Микросервис "Customer": Управляет данными клиентов, используя базу данных PostgreSQL и также взаимодействует с Kafka для отправки уведомлений.
4. Kafka: Служит брокером сообщений для асинхронной отправки уведомлений между микросервисами.
5. Микросервис "Notification": Отправляет уведомления через внешние сервисы, такие как Twilio и Firebase. Хранит данные в базе данных PostgreSQL.
6. Частный Docker-реестр: Хранит образы Docker для развертывания микросервисов.
7. Сервер Eureka: Управляет регистрацией и обнаружением микросервисов.
8. Config Server: Предоставляет конфигурации окружения для микросервисов.
9. Sleuth и Zipkin: Реализуют распределенное трассирование для мониторинга и отладки взаимодействий между микросервисами.

## Архитектура:
![image](https://github.com/AntonRudnikovskiy/SentinelGuard/assets/109467887/b9004141-9c5e-4284-9be9-93f9e524f1d2)
