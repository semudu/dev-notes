# Java 8 - Yeni Özellikler

## 1. Lambda İfadeleri
Fonksiyonel programlamayı destekler, kodun daha kısa ve okunabilir olmasını sağlar.
```java
List<String> list = Arrays.asList("a", "b", "c");
list.forEach(item -> System.out.println(item));
```

## 2. Stream API
Koleksiyonlar üzerinde fonksiyonel işlemler yapılmasına olanak tanır.
```java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
int toplam = numbers.stream().filter(n -> n % 2 == 0).mapToInt(Integer::intValue).sum();
```

## 3. Yeni Tarih/Zaman API’si (java.time)
Modern ve güvenli tarih/zaman işlemleri sağlar.
```java
import java.time.LocalDate;
LocalDate today = LocalDate.now();
```

## 4. Varsayılan ve Statik Arayüz Metotları
Arayüzlerde gövdesi olan metotlar tanımlanabilir.
```java
interface MyInterface {
    default void hello() { System.out.println("Hello"); }
    static void bye() { System.out.println("Bye"); }
}
```

## 5. Optional Sınıfı
NullPointerException riskini azaltır.
```java
Optional<String> isim = Optional.ofNullable(null);
System.out.println(isim.orElse("Varsayılan"));
```

## 6. Paralel Stream
Veri işleme işlemlerini paralel olarak gerçekleştirebilir.
```java
int toplam = numbers.parallelStream().mapToInt(Integer::intValue).sum();
```

Daha fazla detay ve örnekler için diğer dosyalara bakınız.
