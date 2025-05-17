# Java 11 - Geçiş ve Uyumluluk Notları

## Geçişte Dikkat Edilmesi Gerekenler

- Java 8’den Java 11’e geçerken bazı eski API’ler ve modüller kaldırılmıştır (ör. Java EE, CORBA).
- JavaFX artık JDK içinde gelmez, ayrı olarak eklenmelidir.
- Bazı komut satırı araçları (javaws, jvisualvm vb.) kaldırılmıştır.
- Minimum çalışma zamanı ve derleyici sürümü Java 11 olmalıdır.

## Uyumluluk Notları

- Kodunuzu Java 11 ile derleyip test edin, özellikle kaldırılan API’leri kullanan bölümleri kontrol edin.
- build araçlarınızı (Maven, Gradle) ve bağımlılıklarınızı güncel tutun.
- Yeni özellikleri (HTTP Client, String/Optional metotları, ZGC) kademeli olarak entegre edin.

## İpuçları

- Eski kodları refactor ederken yeni API’leri kullanmaya özen gösterin.
- Java 11 LTS olduğu için uzun süreli projelerde tercih edilebilir.
- Oracle ve OpenJDK sürümleri arasında lisans ve dağıtım farklarını göz önünde bulundurun.

Daha fazla detay için Oracle’ın resmi migration rehberine bakabilirsiniz.
