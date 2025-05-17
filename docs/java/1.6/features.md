# Java 1.6 (Java 6) - Yeni Özellikler

## 1. Scripting API (JSR 223)
Java uygulamalarında Java dışı dillerin (ör. JavaScript) çalıştırılmasını sağlar.
```java
import javax.script.ScriptEngineManager;
import javax.script.ScriptEngine;

public class ScriptExample {
    public static void main(String[] args) throws Exception {
        ScriptEngineManager manager = new ScriptEngineManager();
        ScriptEngine engine = manager.getEngineByName("JavaScript");
        engine.eval("print('Merhaba Java 6 Scripting!');");
    }
}
```

## 2. Web Servisleri (JAX-WS, JAXB)
SOAP tabanlı web servisleri oluşturmak ve XML ile çalışmak kolaylaştı.

## 3. Compiler API (JSR 199)
Java kodunu çalışma zamanında derlemek mümkün hale geldi.

## 4. Donanım Hızlandırmalı Grafikler
Java 2D ve Direct3D desteği ile grafik işlemleri hızlandı.

## 5. Yönetilebilirlik ve İzleme
Yeni MBeans ve gelişmiş monitoring araçları eklendi.

Daha fazla detay ve örnekler için diğer dosyalara bakınız.
