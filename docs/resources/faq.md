# Sık Sorulan Sorular (FAQ)

Bu bölüm, Java, Spring, cloud-native, DevOps, mimari, troubleshooting ve kariyerle ilgili en sık sorulan soruları ve kısa cevaplarını içerir.

## 1. Java & Spring
- Java ile Spring arasındaki temel fark nedir?
  - Java bir programlama dili, Spring ise Java için geliştirilmiş bir framework’tür.
- Spring Boot ile Spring Framework farkı nedir?
  - Spring Boot, Spring uygulamalarını hızlı ve kolay başlatmak için otomatik konfigürasyon ve starter bağımlılıkları sunar.

## 2. Cloud & DevOps
- Cloud-native uygulama nedir?
  - Bulut ortamında doğrudan çalışacak şekilde tasarlanmış, ölçeklenebilir ve otomatik yönetilebilen uygulamalardır.
- CI/CD nedir?
  - Sürekli entegrasyon (CI) ve sürekli teslimat/deployment (CD) süreçlerini otomatikleştiren yazılım geliştirme yaklaşımıdır.

## 3. Yazılım Mimarisi
- Monolith ve microservices farkı nedir?
  - Monolith tek parça uygulamadır, microservices ise bağımsız deploy edilebilen küçük servislerden oluşur.
- CAP teoremi nedir?
  - Dağıtık sistemlerde aynı anda consistency, availability ve partition tolerance’ın üçünü birden tam olarak sağlamak mümkün değildir.

## 4. Troubleshooting & Best Practices
- Memory leak nedir, nasıl tespit edilir?
  - Kullanılmayan nesnelerin bellekten temizlenmemesiyle oluşur; heap dump ve profiler araçlarıyla tespit edilir.
- N+1 select problemi nedir?
  - ORM ile ilişkili veriler çekilirken her kayıt için ayrı sorgu atılmasıdır; fetch join veya entity graph ile çözülür.

## 5. Güvenlik
- JWT nedir, neden kullanılır?
  - JSON Web Token, stateless authentication için kullanılan bir standarttır.
- Secret management nasıl yapılır?
  - Secrets environment variable, external vault veya config server’da saklanmalı, kodda tutulmamalıdır.

## 6. Kariyer & Gelişim
- Staff engineer, solution architect, cloud architect rolleri arasındaki farklar nelerdir?
  - Staff engineer teknik liderlik ve derin uzmanlık, solution architect çözüm tasarımı, cloud architect ise bulut altyapısı ve mimarisi odaklıdır.
- Mülakatlarda en çok hangi konular sorulur?
  - OOP, concurrency, microservices, cloud, DevOps, security, best practices ve problem çözme.

Her başlık altında yeni sorular ekleyerek blogunuzu güncel tutabilirsiniz.
