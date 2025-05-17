# Spring Test & Mocking

Bu bölüm, Spring uygulamalarında test stratejileri, mocking teknikleri ve test otomasyonu konularını kapsar.

## 1. Unit Test ve Integration Test
- Unit test için @WebMvcTest, @DataJpaTest, @MockBean
- Integration test için @SpringBootTest, gerçek veri tabanı ile test

## 2. Mocking ve Test Double
- Mockito, EasyMock, JMockit ile mocking
- Spy, stub, fake, dummy kavramları

## 3. MockMvc ile REST API Testi
- MockMvc ile controller ve endpoint testleri
- JSON path, request/response validation

## 4. Testcontainers ile Entegre Testler
- Docker tabanlı veri tabanı, message broker, cache test ortamı
- Test lifecycle yönetimi

## 5. Veri Tabanı Testleri
- H2, PostgreSQL, MySQL ile test ortamı
- @Transactional, rollback, test isolation

## 6. Test Coverage ve Otomasyon
- Coverage araçları: JaCoCo, Cobertura
- CI/CD pipeline’da otomatik test çalıştırma

## 7. Test Best Practices
- Deterministic ve repeatable testler
- Test data management, fixture kullanımı
- Flaky test önleme, test maintenance

## 8. Sık Karşılaşılan Sorunlar ve Çözüm Yöntemleri
- Mocking hataları, context caching, test isolation sorunları
- Test performansı ve paralel test çalıştırma

Her başlık altında örnekler, kod parçaları ve ileri seviye detaylar için ilgili alt bölümlere göz atabilirsiniz.
