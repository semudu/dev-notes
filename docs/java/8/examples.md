# Java 8 - Kod Örnekleri

## 1. Lambda İfadeleri ile Liste İşleme
```java
List<String> isimler = Arrays.asList("Ali", "Veli", "Ayşe");
isimler.forEach(isim -> System.out.println(isim));
```

## 2. Stream API ile Filtreleme ve Toplama
```java
List<Integer> sayilar = Arrays.asList(1, 2, 3, 4, 5, 6);
int toplam = sayilar.stream()
    .filter(sayi -> sayi % 2 == 0)
    .mapToInt(Integer::intValue)
    .sum();
System.out.println("Çift sayıların toplamı: " + toplam);
```

## 3. Yeni Tarih/Zaman API Kullanımı
```java
import java.time.LocalDate;
import java.time.format.DateTimeFormatter;

LocalDate bugun = LocalDate.now();
System.out.println(bugun.format(DateTimeFormatter.ofPattern("dd.MM.yyyy")));
```

## 4. Optional ile Null Kontrolü
```java
Optional<String> ad = Optional.ofNullable(null);
System.out.println(ad.orElse("Bilinmiyor"));
```

## 5. Varsayılan Arayüz Metodu
```java
interface Selam {
    default void merhaba() { System.out.println("Merhaba!"); }
}
```

Daha fazla örnek ve açıklama için diğer dosyalara bakınız.
