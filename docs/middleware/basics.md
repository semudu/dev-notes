# Middleware Temel Kavramlar

Bu bölüm, modern kurumsal uygulamalarda kullanılan middleware teknolojilerinin temel yapı taşlarını ve entegrasyon desenlerini açıklar.

## 1. Middleware Nedir?
- Uygulamalar arası iletişimi ve entegrasyonu sağlayan yazılım katmanı
- Message broker, API gateway, service mesh, event bus gibi bileşenler

## 2. Mesajlaşma ve Kuyruk Sistemleri
- Message queue, topic, pub/sub, point-to-point
- Sık kullanılan teknolojiler: RabbitMQ, Kafka, ActiveMQ, IBM MQ

## 3. API Gateway ve Service Mesh
- API yönetimi, rate limiting, authentication, routing
- Service mesh ile servisler arası güvenli ve gözlemlenebilir iletişim (örn. Istio, Linkerd)

## 4. Event-Driven Architecture (EDA)
- Event sourcing, CQRS, event bus
- Asenkron ve reaktif sistemler için temel yapı

## 5. Entegrasyon Desenleri
- Enterprise Integration Patterns (EIP)
- Adapter, transformer, aggregator, splitter, filter gibi desenler

## 6. Middleware Güvenliği ve İzlenebilirlik
- Mesaj şifreleme, kimlik doğrulama, audit log
- Distributed tracing, monitoring, alerting

## 7. Performans ve Ölçeklenebilirlik
- Yük dengeleme, partitioning, backpressure
- Yüksek erişilebilirlik ve felaket kurtarma

## 8. Sık Karşılaşılan Sorunlar ve Çözüm Yöntemleri
- Mesaj kaybı, duplicate delivery, ordering problemleri
- Bağlantı ve network sorunları

Her başlık altında örnekler, mimari diyagramlar ve ileri seviye detaylar için ilgili alt bölümlere göz atabilirsiniz.
