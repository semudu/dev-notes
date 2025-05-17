# Domain-Driven Design (DDD)

Bu bölüm, karmaşık iş alanlarında yazılım tasarımını kolaylaştırmak için kullanılan Domain-Driven Design (DDD) yaklaşımını ve uygulama örneklerini kapsar.

## 1. DDD Nedir?
- İş alanı (domain) odaklı modelleme
- Teknik ve iş ekipleri arasında ortak dil (ubiquitous language)

## 2. Temel Kavramlar
- Entity: Kimliği olan nesne
- Value Object: Kimliği olmayan, değeriyle tanımlanan nesne
- Aggregate: Transactional boundary, aggregate root
- Repository: Aggregate erişimi için soyutlama
- Service: Domain logic’in aggregate dışında modellenmesi

## 3. Bounded Context ve Context Mapping
- Bounded context: Modelin sınırları, context haritalama
- Context map: Shared kernel, customer/supplier, conformist, anti-corruption layer

## 4. Event Storming ve Domain Event’ler
- İş süreçlerinin event’lerle modellenmesi
- Event storming workshop’ları, event sourcing

## 5. Implementation Patterns
- Layered architecture, hexagonal architecture ile DDD
- Application service, domain service, infrastructure layer

## 6. Microservices ve DDD
- Her bounded context’in ayrı bir mikroservis olması
- Veri tutarlılığı, eventual consistency, saga pattern

## 7. Best Practices ve Sık Karşılaşılan Sorunlar
- Model karmaşıklığı, context sınırlarının belirlenmesi
- Ubiquitous language’in sürdürülebilirliği

Her başlık altında örnekler, diyagramlar ve ileri seviye detaylar için ilgili alt bölümlere göz atabilirsiniz.
