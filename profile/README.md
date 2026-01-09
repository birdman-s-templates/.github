# QA Automation Templates 

Коллекция шаблонов и примеров для автоматизации тестирования на Python.

## Репозитории в коллекции

### 1. [common](https://github.com/birdman93/common)
**Кросспроектная библиотека с общими обвязками**

Общая библиотека, которая обеспечивает переиспользуемые компоненты для всех других репозиториев.

**Включает:**
- **bindings** — интеграция с сервисами:
  - Kerberos для аутентификации
  - Vault для управления secrets
  - Logger с автоматическим определением имён функций
  - Работа с СУБД: PostgreSQL, Cassandra, Dragonfly, Aerospike
  - Kafka для работы с message streams (encoders/decoders)

- **utils** — утилиты общего назначения:
  - Non-blocking asserts для асинхронных проверок
  - State management для управления состоянием
  - Tags для маркирования и фильтрации тестов

**Ключевая особенность:**
Централизованное управление всеми интеграциями позволяет легко обновлять зависимости и поддерживать консистентность кода во всех проектах.

**Стек:**
- Python 3.x
- pytest
- Apache Kafka (+ Kerberos)
- Aerospike
- Cassandra
- Dragonfly
- PostrgeSQL
- Vault

---

### 2. [functional-test-template](https://github.com/birdman93/functional-test-template)
**Пример функционального тестирования REST API сервиса, предназначенного для создания kafka-to-kafka потоков**

**Стек:**
- Python 3.x
- pytest
- PostrgeSQL
- Apache Kafka

**Структура тестов:**
```
tests/
└── shrinker_domain/
    ├── calls/
    ├── geo/
    ├── roaming/
    ├── sms/
    └── url/
```

---

### 3. [load-test-template](https://github.com/birdman93/load-test-template)
**Пример скрипта для нагрузочного тестирования GraphQL API**

Готовый к использованию шаблон для нагрузочного тестирования GraphQL эндпоинтов с использованием **Locust**.

**Ключевые особенности:**
- Множественные сценарии нагрузки (full_data, mixed_sample, slow_data, fast_data и т.д.)
- Работа с несколькими окружениями (prep1, dev1, test1, prod1, prod1_ip)
- Гибкая система параметров запуска (--scenario, --endpoint, --db-limit, --api-env)
- Динамическая генерация GraphQL запросов из схемы

**Стек:**
- Python 3.x
- Locust
- Cassandra
- Dragonfly

---

### 4. [generator-for-the-load-stand](https://github.com/birdman93/generator-for-the-load-stand)
**Генератор синтетических данных для нагрузочного стенда**

Специализированный инструмент для создания и подготовки синтетических данных для нагрузочного тестирования.

**Ключевые особенности:**
- Генерация репрезентативных тестовых данных
- Интеграция с различными хранилищами (Cassandra, Dragonfly)
- Поддержка массовой загрузки данных

**Стек:**
- Python 3.x
- Cassandra
- Dragonfly

---

## Дополнительные ресурсы

Каждый репозиторий содержит подробный `README.md` с:
- Описанием архитектуры
- Примерами использования
- Рекомендациями по конфигурации
- Troubleshooting гайдом

---
