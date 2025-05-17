# Java 21 - Yeni Özellikler ve Derinlemesine Açıklamalar

## 1. Record Patterns ve Pattern Matching for switch
### 1.1 Record Patterns
- Record veri tiplerinde desen eşleme ile alanlara doğrudan erişim.
- Kodun okunabilirliğini ve güvenliğini artırır.

### 1.2 Pattern Matching for switch
- Switch ifadelerinde gelişmiş desen eşleme.
- Farklı veri tiplerinin ayrıştırılması ve işlenmesi kolaylaşır.

## 2. Virtual Threads (Project Loom)
### 2.1 Hafif ve Yüksek Ölçeklenebilir Thread’ler
- Binlerce thread’i düşük maliyetle başlatma.
- Geleneksel thread’lere göre daha az kaynak tüketimi.
- Paralel ve eşzamanlı programlamada devrim.

### 2.2 Kullanım Senaryosu
- Yüksek trafikli sunucular, mikroservisler, reaktif olmayan IO işlemleri.

## 3. String Templates
### 3.1 Güvenli ve Okunabilir String Birleştirme
- Gömülü ifadelerle dinamik string oluşturma.
- SQL, JSON gibi dış formatlara güvenli veri gömme.
- Compile-time kontrol ve otomatik escaping.

## 4. Foreign Function & Memory API (FFM)
### 4.1 Native Kod ile Etkileşim
- JNI’ye göre daha güvenli ve kolay native kütüphane çağrıları.
- C/C++ fonksiyonlarına doğrudan erişim.

### 4.2 Bellek Yönetimi
- Java heap dışı bellekle güvenli çalışma.
- Zero-copy veri paylaşımı ve yüksek performans.

## 5. Platform Güvenliği ve Performans
### 5.1 GC ve Memory Leak Tespiti
- Yeni GC seçenekleri ve memory leak tespiti.
- TLS/SSL güncellemeleri, güvenlik açıklarının kapatılması.

## 6. Preview ve Incubator Özellikler
### 6.1 Yeni Dil ve API Denemeleri
- unnamed variables, unnamed patterns gibi geleceğe yönelik dil denemeleri.
- Gelecekteki Java sürümlerine hazırlık.

Her başlık altında örnekler ve kullanım detayları için examples.md dosyasına bakınız.
