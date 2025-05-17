# Kişisel Notlar

Bu bölüm, yazılım geliştirme sürecinde edinilen kişisel notlar, önemli ipuçları, sık kullanılan komutlar ve pratik önerileri içerir.

## 1. Sık Kullanılan Komutlar
- Maven build: `mvn clean install`
- Gradle build: `./gradlew build`
- Docker image build: `docker build -t myapp .`
- Kubernetes deploy: `kubectl apply -f deployment.yaml`
- Git stash: `git stash && git stash pop`

## 2. Kod Snippet’leri
- Java stream ile filtreleme:
  ```java
  list.stream().filter(x -> x.isActive()).collect(Collectors.toList());
  ```
- Spring Boot health endpoint:
  ```yaml
  management:
    endpoints:
      web:
        exposure:
          include: health,info
  ```

## 3. Troubleshooting İpuçları
- Heap dump almak için: `jmap -dump:live,format=b,file=heap.bin <pid>`
- Thread dump almak için: `jstack <pid>`
- Docker container logları: `docker logs <container_id>`

## 4. Öğrenilen Dersler & Pratik Öneriler
- Her zaman test yaz, kodunu küçük parçalara böl.
- Konfigürasyonları koddan ayır, environment variable kullan.
- Monitoring ve alerting’i production’a geçmeden kur.
- Kodun okunabilirliğine ve dokümantasyonuna önem ver.
- “Works on my machine” demek yerine CI/CD pipeline’da test et.

## 5. Faydalı Kısa Notlar
- JVM tuning için Xms/Xmx değerlerini uygulamanın ihtiyacına göre ayarla.
- Spring Boot’ta profile bazlı konfigürasyon için `@Profile` annotation kullan.
- Kubernetes’te resource limitlerini belirle, aksi halde node’lar dolabilir.

Her başlık altında kendi deneyimlerinizi ve yeni notlarınızı ekleyerek blogunuzu kişiselleştirebilirsiniz.
