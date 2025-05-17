# Java 24 - Yeni Özellikler ve Derinlemesine Açıklamalar

## 1. Scoped Values ve Structured Concurrency
### 1.1 Scoped Values
- Thread-local değişkenlerin daha güvenli ve kontrollü yönetimi.
- Özellikle virtual threads ile birlikte veri izolasyonu sağlar.
- Yan etkisiz, fonksiyonel programlama ile uyumlu.

### 1.2 Structured Concurrency
- Paralel işlemlerin yaşam döngüsünü yönetmek için yeni bir model.
- Alt görevlerin ana görevle birlikte başlatılıp, birlikte sonlandırılması.
- Hataların ve istisnaların daha kolay yönetilmesi.

## 2. String Templates (Kararlı)
- String birleştirme ve gömülü ifadeler için yeni, güvenli ve okunabilir bir sözdizimi.
- SQL, JSON gibi dış formatlara güvenli veri gömme.
- Compile-time kontrol ve otomatik escaping.

## 3. Class-File API
- Bytecode üzerinde programatik değişiklik ve analiz imkanı.
- Derleyici ve araç geliştiriciler için düşük seviyede kontrol.
- Reflection’dan daha hızlı ve güvenli.

## 4. Foreign Function & Memory API (FFM)
### 4.1 Native Kod ile Etkileşim
- JNI’ye göre daha güvenli ve kolay native kütüphane çağrıları.
- C/C++ fonksiyonlarına doğrudan erişim.

### 4.2 Bellek Yönetimi
- Java heap dışı bellekle güvenli çalışma.
- Zero-copy veri paylaşımı ve yüksek performans.

## 5. Virtual Threads ve Paralel Programlama
- Binlerce thread’i düşük maliyetle başlatma imkanı.
- Yüksek ölçeklenebilirlik ve reaktif programlamaya alternatif.

## 6. Platform Güvenliği ve Performans
- Yeni GC iyileştirmeleri, memory leak tespiti.
- Güvenlik açıklarının kapatılması, TLS/SSL güncellemeleri.

## 7. Preview ve Incubator Özellikler
- Yeni dil ve API denemeleri (örn. unnamed variables, unnamed patterns).
- Gelecekteki Java sürümlerine hazırlık.

Her başlık altında örnekler ve kullanım senaryoları için examples.md dosyasına bakınız.
