# Event-Driven Architecture

Bu bölüm, event-driven mimarinin temel kavramlarını, avantajlarını, uygulama desenlerini ve best practices’i kapsar.

## 1. Event-Driven Architecture Nedir?
- Olay tabanlı iletişim, loosely coupled sistemler
- Producer, consumer, event bus, event store kavramları

## 2. Event Sourcing ve CQRS
- Event sourcing ile veri değişikliklerinin event olarak saklanması
- Command Query Responsibility Segregation (CQRS) ile okuma/yazma ayrımı

## 3. Event Bus ve Messaging
- Event bus, message broker, pub/sub, topic, queue
- Kafka, RabbitMQ, ActiveMQ ile event-driven uygulama geliştirme

## 4. Async Processing ve Scalability
- Asenkron event işleme, worker pool, backpressure yönetimi
- Event replay, idempotency, ordering

## 5. Integration Patterns
- Saga pattern, process manager, compensating transaction
- Event choreography vs orchestration

## 6. Monitoring ve Observability
- Event tracing, distributed logging, metrics
- Dead letter queue, alerting, event replay

## 7. Best Practices ve Sık Karşılaşılan Sorunlar
- Event schema versioning, backward compatibility
- Event loss, duplicate event, eventual consistency

Her başlık altında örnekler, mimari diyagramlar ve ileri seviye detaylar için ilgili alt bölümlere göz atabilirsiniz.
