# Java & JVM Troubleshooting

Bu bölüm, Java ve JVM tabanlı uygulamalarda sık karşılaşılan sorunların tespiti, analizi ve çözüm yöntemlerini içerir.

## 1. JVM Tuning ve Performans Analizi
- JVM parametreleri, heap ve stack ayarları
- Profiling araçları: VisualVM, JMC, YourKit, Flight Recorder
- GC log analizi ve tuning (G1, ZGC, Parallel GC)

## 2. Memory Leak ve OutOfMemoryError
- Heap dump alma ve analiz etme
- Leak tespiti için MAT, Eclipse Memory Analyzer kullanımı
- Kodda sık yapılan memory leak hataları

## 3. Thread Deadlock ve Concurrency Sorunları
- Thread dump alma ve analiz etme
- Deadlock, livelock, starvation tespiti
- Senkronizasyon ve lock yönetimi

## 4. Garbage Collection Sorunları
- GC tuning, stop-the-world analizleri
- Promotion failure, fragmentation, excessive GC cycles

## 5. ClassLoader ve Bağımlılık Çatışmaları
- ClassNotFoundException, NoClassDefFoundError
- Farklı classloader’lar ve shadowing sorunları

## 6. Performans ve Latency Problemleri
- CPU, IO, network bottleneck tespiti
- JIT compiler ve hotspot optimizasyonları

## 7. Hata Ayıklama ve Log Analizi
- Exception stack trace okuma ve root cause analizi
- Log seviyeleri, log correlation, distributed tracing

## 8. Sık Karşılaşılan Hatalar ve Çözüm Yöntemleri
- NullPointerException, ConcurrentModificationException, StackOverflowError
- Bağımlılık yönetimi ve versiyon uyumsuzlukları

Her başlık altında örnekler, araç kullanımı ve ileri seviye detaylar için ilgili alt bölümlere göz atabilirsiniz.
