# Spring Troubleshooting

Bu bölüm, Spring ve Spring Boot projelerinde sık karşılaşılan sorunların tespiti, analizi ve çözüm yöntemlerini kapsar.

## 1. Konfigürasyon ve Property Sorunları
- Property injection hataları, profile yönetimi
- Config server ve centralized config sorunları

## 2. Dependency ve Bean Initialization Hataları
- Circular dependency, unsatisfied dependency
- BeanNotOfRequiredTypeException, NoSuchBeanDefinitionException

## 3. Bean Lifecycle ve Scope Problemleri
- Singleton vs prototype scope, bean destruction
- @PostConstruct, @PreDestroy, lifecycle callback hataları

## 4. Security ve Authentication Problemleri
- CSRF, CORS, session management hataları
- JWT/OAuth2 authentication sorunları

## 5. Transaction ve Persistence Sorunları
- Transaction propagation, rollback, nested transaction hataları
- LazyInitializationException, N+1 select problemi

## 6. Test ve Mocking Sorunları
- MockMvc, Testcontainers, context caching hataları
- Test isolation, flaky test, test data management

## 7. Deployment ve Environment Problemleri
- Port çakışmaları, environment variable eksikliği
- Health check, actuator endpoint erişim sorunları

## 8. Performans ve Memory Problemleri
- Memory leak, thread pool exhaustion, slow startup
- Profiling ve monitoring ile root cause analizi

Her başlık altında örnekler, araç kullanımı ve ileri seviye detaylar için ilgili alt bölümlere göz atabilirsiniz.
