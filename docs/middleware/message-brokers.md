# Message Brokers

Bu bölüm, modern kurumsal uygulamalarda kullanılan mesajlaşma altyapıları ve message broker teknolojilerini kapsar.

## 1. Message Broker Nedir?
- Uygulamalar arası asenkron iletişim ve entegrasyon
- Queue, topic, pub/sub, point-to-point kavramları

## 2. RabbitMQ
- AMQP protokolü, exchange, queue, binding
- Routing, dead letter queue, priority queue
- Management UI, monitoring, clustering

## 3. Apache Kafka
- Distributed commit log, topic, partition, consumer group
- High throughput, scalability, event streaming
- Exactly-once delivery, retention, compaction

## 4. ActiveMQ ve IBM MQ
- JMS desteği, persistent/non-persistent delivery
- Transaction management, message selector
- Enterprise integration ve legacy sistemlerle uyum

## 5. Delivery Guarantees ve Mesaj Güvenliği
- At least once, at most once, exactly once delivery
- Message ordering, idempotency, duplicate detection

## 6. Ölçeklenebilirlik ve Yüksek Erişilebilirlik
- Partitioning, replication, failover, clustering
- Load balancing, horizontal scaling

## 7. Monitoring ve Troubleshooting
- Metrics, alerting, dead letter queue analizi
- Message tracing, slow consumer detection

## 8. Best Practices ve Sık Karşılaşılan Sorunlar
- Backpressure yönetimi, message size limiti
- Network partition, message loss, recovery stratejileri

Her başlık altında örnekler, mimari diyagramlar ve ileri seviye detaylar için ilgili alt bölümlere göz atabilirsiniz.
