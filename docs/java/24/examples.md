# Java 24 - Kod Örnekleri ve Kullanım Senaryoları

## 1. Scoped Values ve Structured Concurrency

### 1.1 Scoped Values Kullanımı
```java
import java.lang.ScopedValue;

public class ScopedValueExample {
    static final ScopedValue<String> USER = ScopedValue.newInstance();

    public static void main(String[] args) {
        ScopedValue.where(USER, "admin").run(() -> {
            System.out.println("Kullanıcı: " + USER.get());
        });
    }
}
```
ScopedValue ile thread-local değişkenlerin güvenli yönetimi.

### 1.2 Structured Concurrency ile Paralel Görevler
```java
import java.util.concurrent.StructuredTaskScope;

try (var scope = new StructuredTaskScope.ShutdownOnFailure()) {
    scope.fork(() -> fetchData());
    scope.fork(() -> processData());
    scope.join();
}
```
Alt görevlerin birlikte başlatılıp, birlikte yönetilmesi.

## 2. String Templates
```java
String ad = "Ali";
int yas = 30;
String bilgi = STR."Ad: \{ad}, Yaş: \{yas}";
System.out.println(bilgi);
```
Güvenli ve okunabilir string birleştirme.

## 3. Class-File API ile Bytecode Analizi
```java
import java.lang.classfile.ClassFile;
import java.nio.file.Path;

ClassFile cf = ClassFile.read(Path.of("MyClass.class"));
cf.methods().forEach(m -> System.out.println(m.name()));
```
Bytecode üzerinde programatik analiz ve işlem.

## 4. Foreign Function & Memory API (FFM)

### 4.1 Native Fonksiyon Çağrısı
```java
import java.foreign.*;
import java.foreign.memory.*;

try (MemorySegment segment = MemorySegment.allocateNative(100)) {
    // Native kütüphane ile çalışma örneği
}
```

### 4.2 Bellek Yönetimi
Java heap dışı bellekle güvenli çalışma ve veri paylaşımı.

## 5. Virtual Threads ile Yüksek Ölçeklenebilirlik
```java
Runnable task = () -> System.out.println("Sanal thread!");
Thread.startVirtualThread(task);
```
Binlerce thread’i düşük maliyetle başlatma.

## 6. Preview ve Incubator Özellikler
```java
// Unnamed variables (preview)
(int _, int y) -> y * 2;
```
Yeni dil denemeleri ve geleceğe hazırlık.

Her örneğin detaylı açıklamaları ve kullanım ipuçları için features.md dosyasına bakınız.
