# Java 11 - Yeni Özellikler ve Derinlemesine Açıklamalar

## 1. HTTP Client API
### 1.1 Modern HTTP/2 ve WebSocket Desteği
- Yerleşik, asenkron ve senkron HTTP istekleri.
- WebSocket ile gerçek zamanlı iletişim.
- RESTful servislerle kolay entegrasyon.

### 1.2 Kullanım Senaryosu
- API istemcileri, mikroservisler, veri çekme ve entegrasyon projeleri.

## 2. String, Collection ve Optional Geliştirmeleri
### 2.1 String Sınıfı
- `isBlank()`, `lines()`, `strip()`, `repeat()` gibi yeni metotlar.
- Metin işleme ve veri temizleme işlemlerinde kolaylık.

### 2.2 Collection API
- `copyOf()`, `toArray(IntFunction<T[]>)` ile immutable koleksiyonlar ve kolay dönüşümler.

### 2.3 Optional Sınıfı
- `isEmpty()`, `ifPresentOrElse()` ile null güvenliği ve fonksiyonel kullanım.

## 3. Lambda Parametrelerinde var Anahtar Kelimesi
- Lambda ifadelerinde parametre tipi olarak `var` kullanılabilir.
- Tip çıkarımı ve anotasyon desteği.

## 4. Z Garbage Collector (ZGC)
### 4.1 Düşük Gecikmeli Çöp Toplayıcı
- Büyük heap’lerde düşük gecikme ile bellek yönetimi.
- Özellikle yüksek performans gerektiren sunucu uygulamalarında avantaj.

## 5. JavaFX’in JDK’dan Ayrılması
- JavaFX artık ayrı bir modül olarak sunuluyor.
- Masaüstü uygulamalarında modülerlik ve bağımsız güncelleme imkanı.

## 6. Diğer JEP ve API Geliştirmeleri
### 6.1 Dosya Okuma/Yazma Kolaylıkları
- Yeni dosya API’leri ile hızlı ve güvenli dosya işlemleri.

### 6.2 Flight Recorder ve Mission Control
- Uygulama izleme, performans analizi ve hata tespiti için gelişmiş araçlar.

### 6.3 Güvenlik ve Performans
- TLS/SSL güncellemeleri, güvenlik açıklarının kapatılması.

Her başlık altında örnekler ve kullanım detayları için examples.md dosyasına bakınız.
