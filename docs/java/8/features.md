# Java 8 - Yeni Özellikler ve Derinlemesine Açıklamalar

## 1. Lambda İfadeleri
### 1.1 Fonksiyonel Programlama Desteği
- Fonksiyonları değişken olarak kullanabilme.
- Kodun daha kısa, okunabilir ve fonksiyonel olmasını sağlar.
- Özellikle koleksiyon işlemlerinde büyük kolaylık.

### 1.2 Kullanım Senaryosu
- Event handling, callback, koleksiyon işlemleri.

## 2. Stream API
### 2.1 Fonksiyonel Koleksiyon İşlemleri
- Map, filter, reduce gibi fonksiyonel işlemler.
- Zincirleme veri işleme ve pipeline oluşturma.

### 2.2 Paralel Stream
- Büyük veri setlerinde paralel işleme ile performans artışı.
- Thread yönetimi otomatik olarak yapılır.

## 3. Yeni Tarih/Zaman API’si (java.time)
### 3.1 Modern ve Güvenli Tarih/Zaman İşlemleri
- Immutable ve thread-safe tarih/zaman nesneleri.
- LocalDate, LocalTime, ZonedDateTime gibi yeni sınıflar.

### 3.2 Kullanım Senaryosu
- Zaman dilimi yönetimi, tarih aritmetiği, formatlama/parsing.

## 4. Varsayılan ve Statik Arayüz Metotları
### 4.1 Default Methods
- Arayüzlerde gövdeli metot tanımlama.
- Geriye dönük uyumluluk ve API evrimi.

### 4.2 Static Methods
- Arayüzde yardımcı metotların doğrudan tanımlanabilmesi.

## 5. Optional Sınıfı
### 5.1 Null Güvenliği
- NullPointerException riskini azaltır.
- Değerin olup olmadığını fonksiyonel olarak kontrol etme.

### 5.2 Kullanım Senaryosu
- API dönüşlerinde null yerine Optional kullanımı.

Her başlık altında örnekler ve kullanım detayları için examples.md dosyasına bakınız.
