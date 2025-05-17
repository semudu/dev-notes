# Java 17 - Kod Örnekleri

## 1. Pattern Matching for switch
```java
Object obj = "Merhaba";
switch (obj) {
    case String s -> System.out.println("String: " + s);
    case Integer i -> System.out.println("Integer: " + i);
    default -> System.out.println("Bilinmeyen tip");
}
```

## 2. Sealed Classes
```java
public sealed class Hayvan permits Kedi, Kopek {}
final class Kedi extends Hayvan {}
final class Kopek extends Hayvan {}
```

## 3. Stream.toList()
```java
List<String> list = Stream.of("a", "b", "c").toList();
```

## 4. Foreign Function & Memory API (Preview)
Java dışı kütüphanelerle güvenli etkileşim için yeni API.

## 5. RandomGenerator API
```java
RandomGenerator rnd = RandomGenerator.getDefault();
int sayi = rnd.nextInt();
```

Daha fazla detay ve örnek için diğer dosyalara bakınız.
