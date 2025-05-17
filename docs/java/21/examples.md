# Java 21 - Kod Örnekleri

## 1. Record Patterns ve Pattern Matching for switch
```java
record Kisi(String ad, int yas) {}
Object obj = new Kisi("Ali", 30);
switch (obj) {
    case Kisi(String ad, int yas) -> System.out.println(ad + " - " + yas);
    default -> System.out.println("Bilinmeyen tip");
}
```

## 2. Virtual Threads (Project Loom)
```java
Thread.startVirtualThread(() -> System.out.println("Sanal thread çalıştı!"));
```

## 3. String Templates
```java
// Java 21 ile string template örneği (preview)
String ad = "Ali";
int yas = 30;
String bilgi = STR."Ad: \{ad}, Yaş: \{yas}";
```

## 4. Foreign Function & Memory API
Java dışı kütüphanelerle ve bellekle güvenli etkileşim için yeni API.

Daha fazla detay ve örnek için diğer dosyalara bakınız.
