# Java 17 - Yeni Özellikler ve Derinlemesine Açıklamalar

## 1. Pattern Matching for switch
### 1.1 Desen Eşleme ile Switch
- Switch ifadelerinde tip kontrolü ve desen eşleme desteği.
- Kodun daha okunabilir ve güvenli olması.
- Özellikle sealed class ve record ile birlikte güçlü kullanım.

### 1.2 Kullanım Senaryosu
- Farklı veri tiplerinin ayrıştırılması, polimorfik işlemler.

## 2. Sealed Classes
### 2.1 Sınıf Hiyerarşisinin Sınırlandırılması
- Sadece izin verilen alt sınıfların türetilebilmesi.
- Güvenli ve öngörülebilir miras yapısı.

### 2.2 Kullanım Senaryosu
- API tasarımı, domain modelleme, polimorfizm.

## 3. Yeni Garbage Collector Seçenekleri
### 3.1 G1, ZGC, Shenandoah
- Modern, düşük gecikmeli ve yüksek performanslı çöp toplayıcılar.
- Büyük ölçekli uygulamalarda bellek yönetimi avantajı.

## 4. Strongly Encapsulated JDK Internals
### 4.1 Kapsülleme ve Modülerlik
- JDK iç yapılarının dışarıya kapatılması.
- Güvenlik ve bakım kolaylığı.

## 5. Foreign Function & Memory API (Preview)
### 5.1 Native Kod ile Etkileşim
- JNI’ye göre daha güvenli ve kolay native kütüphane çağrıları.
- Java dışı kodlarla hızlı ve güvenli entegrasyon.

### 5.2 Bellek Yönetimi
- Java heap dışı bellekle güvenli çalışma.

## 6. Deprecation ve Kaldırılan Özellikler
### 6.1 Applet API, Security Manager
- Eski teknolojilerin kaldırılması veya kullanımdan kaldırılması.
- Modern güvenlik ve uygulama mimarilerine geçiş.

## 7. Küçük Dil ve API Geliştirmeleri
### 7.1 Stream.toList(), RandomGenerator API
- Koleksiyon işlemlerinde kolaylık.
- Yeni rastgele sayı üreticileri.

### 7.2 Yeni String ve Collection Metotları
- Kodun okunabilirliğini ve güvenliğini artıran küçük iyileştirmeler.

Her başlık altında örnekler ve kullanım detayları için examples.md dosyasına bakınız.
