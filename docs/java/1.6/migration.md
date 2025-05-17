# Java 1.6 (Java 6) - Geçiş ve Uyumluluk Notları

## Geçişte Dikkat Edilmesi Gerekenler

- Java 1.5 (5) ile büyük oranda geriye dönük uyumluluk sağlanmıştır.
- Bazı eski API’ler deprecated (kullanımdan kaldırılmış) olabilir, güncel dokümantasyon kontrol edilmeli.
- JVM ve JDK güncellemeleriyle birlikte performans ve güvenlik iyileştirmeleri gelir, bu nedenle eski JVM sürümleriyle test yapılmalı.

## Uyumluluk Notları

- 1.6 ile gelen yeni API’ler ve özellikler, eski projelerde kullanılmak istenirse minimum derleyici ve çalışma zamanı sürümü güncellenmeli.
- Özellikle scripting ve web servisleri gibi yeni modüller için ek bağımlılıklar gerekebilir.

## İpuçları

- Kodunuzu derlemeden önce eski ve yeni sürümde test edin.
- build araçlarınızı (Ant, Maven) güncel tutun.
- JVM parametrelerini ve garbage collector ayarlarını gözden geçirin.

Daha fazla detay için Oracle’ın resmi migration rehberine bakabilirsiniz.
