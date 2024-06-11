![image](https://github.com/AntonRudnikovskiy/SentinelGuard/assets/109467887/7805f3fa-dea1-4567-8f87-b5e0fd3c2d38)![image](https://github.com/AntonRudnikovskiy/SentinelGuard/assets/109467887/76fd3e68-3f8b-48e2-8b74-ebebd156aed2)# SentinelGuard

## Описание
SentinelGuard - это проект, предназначенный для обеспечения безопасного и эффективного управления клиентскими и мошенническими данными с использованием микросервисной архитектуры. Основные компоненты проекта включают в себя:

 ##
1. Балансировщик нагрузки: Обеспечивает равномерное распределение входящих запросов между микросервисами для повышения отказоустойчивости и производительности.
2. Микросервис "Fraud": Отвечает за обработку данных, связанных с мошенничеством. Хранит данные в базе данных MongoDB и взаимодействует с Kafka для асинхронной отправки уведомлений.
3. Микросервис "Customer": Управляет данными клиентов, используя базу данных PostgreSQL и также взаимодействует с Kafka для отправки уведомлений.
4. Kafka: Служит брокером сообщений для асинхронной отправки уведомлений между микросервисами.
5. Микросервис "Notification": Отправляет уведомления через внешние сервисы, такие как Twilio и Firebase. Хранит данные в базе данных PostgreSQL.
6. Частный Docker-реестр: Хранит образы Docker для развертывания микросервисов.
7. Сервер Eureka: Управляет регистрацией и обнаружением микросервисов.
8. Config Server: Предоставляет конфигурации окружения для микросервисов.
9. Sleuth и Zipkin: Реализуют распределенное трассирование для мониторинга и отладки взаимодействий между микросервисами.

## Технологии
- Java
- Spring Boot
- Spring Cloud
- Spring Data
- RabbitMQ
- PostgreSQL
- Docker
- Zipkin
- Liquibase
- Sleuth
- Eureka

## Архитектура:
![image](https://github.com/AntonRudnikovskiy/SentinelGuard/assets/109467887/cc4e4d00-1de3-43d9-9a82-7d663af2dc7a)

